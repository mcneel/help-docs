Sets the default time and number of passes constraints. The default recommended setting is to set these render constraints off and let the render engine continue until it is closed or manually stopped. These may be changed using the controls in the Render Window. Setting the Number of passes and Time to 0 allows the rendering to continue until you click Stop Rendering.

#### Time
Specifies the amount of time in Hours/Minutes/Seconds the render will continue to process. Note : The rendering stops after the last pass after the time limit has been reached. If you click Resume Rendering, the rendering will continue for one additional pass.

#### Number of passes
Specifies the number of rendering passes the render will process. Note : Any time you click Resume Rendering, the counter for the number of passes is reset. For example, if you set the number of passes to 10 and stop the rendering after pass 8, the rendering will continue until it reaches 18 passes. Normally renderings may take 10 - 15 passes to start to converge. Architectural interiors may need up to 30 passes to start to converge.
