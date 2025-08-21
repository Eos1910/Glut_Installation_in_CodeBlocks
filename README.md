# Glut_Installation_in_CodeBlocks

<h2>🔧 GLUT Installation for Code::Blocks (Windows)</h2>

<ol>
  <li>Download and install <strong>Code::Blocks</strong>.</li>
  <li>
    Go to this link and download the ZIP file:<br>
    <a href="https://www.transmissionzero.co.uk/software/freeglut-devel/" target="_blank">https://github.com/Goblin80/glut-install</a><br>
    OR use the official FreeGLUT download:<br>
    <a href="http://freeglut.sourceforge.net/index.php" target="_blank">freeglut.sourceforge.net</a><br>
    Extract the zip file after downloading.
  </li>
  <li>
    <strong>Modify Code::Blocks Templates:</strong>
    <ol>
      <li>Run Notepad as administrator.</li>
      <li>Open: <code>C:\Program Files (x86)\CodeBlocks\share\CodeBlocks\templates</code>. Show all files.</li>
      <li>Open <code>glut.cbp</code> and replace all <code>glut32</code> with <code>freeglut</code>.</li>
      <li>Also edit <code>wizard.script</code> located at:<br>
        <code>C:\Program Files (x86)\CodeBlocks\share\CodeBlocks\templates\wizard\glut</code><br>
        Replace <code>glut32</code> with <code>freeglut</code> in this file too.
      </li>
    </ol>
  </li>
  <li>
    <strong>Copy FreeGLUT Files:</strong>
    <ol>
      <li>From <code>freeglut\include\GL</code> → Copy all four header files to:<br>
        <code>C:\Program Files (x86)\CodeBlocks\MinGW\include\GL</code>
      </li>
      <li>From <code>freeglut\lib</code> → Copy the two <code>.a</code> files to:<br>
        <code>C:\Program Files (x86)\CodeBlocks\MinGW\lib</code>
      </li>
      <li>From <code>freeglut\bin</code> → Copy <code>freeglut.dll</code> to:<br>
        <code>C:\Windows\SysWOW64</code>
      </li>
    </ol>
  </li>
  <li>
    <strong>Launch Code::Blocks</strong>:
    <ol>
      <li>File → New → Project → GLUT project → Next</li>
      <li>Choose project title → Next</li>
      <li>Select location: <code>C:\Program Files (x86)\CodeBlocks\MinGW</code></li>
      <li>Press OK → Next → Finish</li>
    </ol>
  </li>
</ol>

<h3>📥 Code::Blocks & MinGW Setup Resources</h3>
<ul>
  <li><a href="https://www.codeblocks.org/downloads" target="_blank">Code::Blocks Download</a></li>
  <li><a href="https://www.codewithc.com/how-to-setup-opengl-glut-in-codeblocks/" target="_blank">CodeWithC GLUT Setup Guide</a></li>
  <li><a href="http://www.transmissionzero.co.uk/software/freeglut-devel/" target="_blank">FreeGLUT MinGW Package</a></li>
  <li><a href="https://www.ics.uci.edu/~pattis/common/handouts/mingweclipse/mingw.html" target="_blank">UCI MinGW Guide</a></li>
</ul>

<h3>💡 Notes on OpenGL Libraries</h3>
<p>You’ll need the following libraries and headers for OpenGL development:</p>
<ul>
  <li><strong>GL</strong> – core OpenGL: <code>gl.h</code>, <code>opengl32</code></li>
  <li><strong>GLU</strong> – OpenGL utility: <code>glu.h</code>, <code>glu32</code></li>
  <li><strong>GLUT</strong> – Window/input manager: <code>freeglut.h</code> or <code>glut.h</code>, <code>freeglut</code></li>
  <li><strong>GLEW</strong> – Extension loader: <code>glew.h</code>, <code>glew32</code></li>
</ul>
<p>All headers should go under <code>&lt;MinGW_HOME&gt;\include\GL</code>, and libraries under <code>&lt;MinGW_HOME&gt;\lib</code>.</p>
