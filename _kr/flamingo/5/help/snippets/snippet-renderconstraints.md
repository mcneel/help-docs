Sets the default time and number of passes constraints. The default recommended setting is to set these render constraints off and let the render engine continue until it is closed or manually stopped. These may be changed using the controls in the Render Window. Setting the Number of passes and Time to 0 allows the rendering to continue until you click Stop Rendering.

#### 시간
렌더링이 계속해서 프로세스되는 시간을 시/분/초로 지정합니다. 안내: 시간 제한에 이른 후 마지막 패스를 지나친 후에 렌더링이 중지됩니다. 렌더링 다시 시작을 클릭하면 추가적으로 한 번의 패스를 계속합니다.

#### 패스의 수
Specifies the number of rendering passes the render will process. Note : Any time you click Resume Rendering, the counter for the number of passes is reset. For example, if you set the number of passes to 10 and stop the rendering after pass 8, the rendering will continue until it reaches 18 passes. Normally renderings may take 10 - 15 passes to start to converge. Architectural interiors may need up to 30 passes to start to converge.
