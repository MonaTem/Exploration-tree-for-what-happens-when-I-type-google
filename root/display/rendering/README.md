Page Rendering
--------------

- Create a 'Frame Tree' or 'Render Tree' by traversing the DOM nodes, and
  calculating the CSS style values for each node.

- Calculate the preferred width of each node in the 'Frame Tree' bottom up
  by summing the preferred width of the child nodes and the node's
  horizontal margins, borders, and padding.

- Calculate the actual width of each node top-down by allocating each node's
  available width to its children.

- Calculate the height of each node bottom-up by applying text wrapping and
  summing the child node heights and the node's margins, borders, and padding.

- Calculate the coordinates of each node using the information calculated
  above.

- More complicated steps are taken when elements are ``floated``,
  positioned ``absolutely`` or ``relatively``, or other complex features
  are used. See
  http://dev.w3.org/csswg/css2/ and http://www.w3.org/Style/CSS/current-work
  for more details.

- Create layers to describe which parts of the page can be animated as a group
  without being re-rasterized. Each frame/render object is assigned to a layer.

- Textures are allocated for each layer of the page.

- The frame/render objects for each layer are traversed and drawing commands
  are executed for their respective layer. This may be rasterized by the CPU
  or drawn on the GPU directly using D2D/SkiaGL.

- All of the above steps may reuse calculated values from the last time the
  webpage was rendered, so that incremental changes require less work.

- The page layers are sent to the compositing process where they are combined
  with layers for other visible content like the browser chrome, iframes
  and addon panels.

- Final layer positions are computed and the composite commands are issued
  via Direct3D/OpenGL. The GPU command buffer(s) are flushed to the GPU for
  asynchronous rendering and the frame is sent to the window server.


  # Notes on GPU Rendering


  * During the rendering process the graphical computing layers can use general
    purpose ``CPU`` or the graphical processor ``GPU`` as well.

  * When using ``GPU`` for graphical rendering computations the graphical
    software layers split the task into multiple pieces, so it can take advantage
    of ``GPU`` massive parallelism for float point calculations required for
    the rendering process.
