<h1 style="text-align:center; font-size:2.5em;">Stealth Game (Unreal Engine)</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Engine-Unreal%20Engine-1f6feb.svg" alt="Unreal Engine Badge"/>
  <img src="https://img.shields.io/badge/Genre-Stealth-blue.svg" alt="Genre Badge"/>
  <img src="https://img.shields.io/badge/Scope-Single%20Level-brightgreen.svg" alt="Scope Badge"/>
  <img src="https://img.shields.io/badge/License-MIT-lightgrey.svg" alt="License Badge"/>
</p>

<p style="font-size:1.1em;">A single-level <b>stealth</b> prototype built with <b>Unreal Engine</b>. This project focuses on basic stealth loop elements—navigation, line-of-sight, and simple AI awareness—organized using typical UE folder structure.</p>

<blockquote><b>Who this is for:</b> Reviewers of my internship portfolio and peers interested in level-focused Unreal prototypes and content organization.</blockquote>

<hr>

<h2>Table of Contents</h2>
<ul>
  <li><a href="#overview">Overview</a></li>
  <li><a href="#features">Key Features</a></li>
  <li><a href="#structure">Project Structure</a></li>
  <li><a href="#getting-started">Getting Started</a></li>
  <li><a href="#play">How to Play</a></li>
  <li><a href="#playtest">Playtest Checklist</a></li>
  <li><a href="#packaging">Packaging for Windows</a></li>
  <li><a href="#design-notes">Design Notes</a></li>
  <li><a href="#future-improvements">Future Improvements</a></li>
  <li><a href="#about-developer">About the Developer</a></li>
  <li><a href="#license">License</a></li>
</ul>

<hr>

<h2 id="overview">Overview</h2>
<p>This repository contains a small Unreal Engine project packaged as a standard UE workspace with <code>Content/</code> and <code>Config/</code> folders plus a <code>.uproject</code> descriptor. It is scoped to one level to emphasize iteration and clarity over size.</p>

<hr>

<h2 id="features">Key Features</h2>
<ul>
  <li><b>Single-level focus:</b> fast iteration on stealth fundamentals.</li>
  <li><b>LoS & awareness hooks:</b> level layout designed for sightlines and cover (blueprint/script hooks ready for expansion).</li>
  <li><b>UE-first structure:</b> assets live under <code>Content/</code>; project settings and input mappings under <code>Config/</code>.</li>
</ul>

<hr>

<h2 id="structure">Project Structure</h2>
<pre>
Stealth_Game/
  Config/                  // Project settings (DefaultEngine.ini, input, etc.)
  Content/                 // Levels, Blueprints, Materials, Meshes, etc.
  GAM303Tutorials.uproject // Unreal project descriptor
</pre>
<p><i>Note:</i> File/folder names reflect typical UE organization; expand as systems grow (e.g., <code>Content/Blueprints/AI</code>, <code>Content/Levels</code>, etc.).</p>

<hr>

<h2 id="getting-started">Getting Started</h2>
<h3>Open in Unreal Editor</h3>
<ol>
  <li>Install <b>Unreal Engine (5.x or your version)</b> via Epic Games Launcher.</li>
  <li>Clone this repository.</li>
  <li>Double-click <code>GAM303Tutorials.uproject</code> to open in the Unreal Editor.<br>
      If prompted, choose <b>Generate Visual Studio project files</b> (Windows) and let UE build shaders.</li>
</ol>

<h3>Build (optional, C++ modules)</h3>
<ol>
  <li>If you add C++ classes, open the generated solution in <b>Visual Studio</b> (or Rider), build the project, then return to the editor.</li>
  <li>Use <b>Play</b> in-editor to run the level.</li>
</ol>

<hr>

<h2 id="play">How to Play</h2>
<p>Default controls follow Unreal templates unless customized in <code>Project Settings &gt; Input</code>:</p>
<ul>
  <li><b>W/A/S/D</b>: Move</li>
  <li><b>Mouse</b>: Look</li>
  <li><b>Shift</b>: Sprint (if enabled)</li>
  <li><b>Ctrl</b>: Crouch (if enabled)</li>
</ul>
<p><i>Tip:</i> For reviewers, you can place a <b>Level Blueprint</b> note or in-world signage describing objectives (reach exit unseen, avoid patrols, etc.).</p>

<hr>

<h2 id="playtest">Playtest Checklist</h2>
<ul>
  <li>Press <code>`</code> to open the console and run <code>stat fps</code> to confirm frame rate stability.</li>
  <li>Test lighting at different scalability levels (<code>Settings → Engine Scalability Settings</code>).</li>
  <li>Enable <code>Show Navigation</code> (P key) to confirm AI pathing coverage.</li>
  <li>Use <code>show collision</code> and <code>show AI</code> to debug visibility and movement boundaries.</li>
  <li>Check for performance spikes when entering/exiting player detection zones.</li>
</ul>

<hr>

<h2 id="packaging">Packaging for Windows</h2>
<ol>
  <li>In the Unreal Editor, go to <b>File → Package Project → Windows → Windows (64-bit)</b>.</li>
  <li>Select a build folder (e.g., <code>Builds/Windows/</code> inside your repo).</li>
  <li>Wait for UE to compile shaders and cook content. When finished, open the output directory.</li>
  <li>Run the generated <code>.exe</code> file to test the standalone version.</li>
  <li>Optional: Compress the folder as a <code>.zip</code> to share with reviewers.</li>
</ol>

<hr>

<h2 id="design-notes">Design Notes</h2>
<ul>
  <li><b>Rapid iteration:</b> single map keeps the focus on layout and feedback loops.</li>
  <li><b>Separation of concerns:</b> content-only until systems demand code; then promote to C++/Blueprint components.</li>
  <li><b>Reviewability:</b> clean folder naming and minimal assets for quick portfolio evaluation.</li>
</ul>

<hr>

<h2 id="future-improvements">Future Improvements</h2>
<ul>
  <li>AI patrol routes with perception (sight/hearing) using <code>AIPerception</code> or <code>Pawn Sensing</code>.</li>
  <li>Player stealth verbs: crouch speed, noise meters, distraction gadgets.</li>
  <li>Simple HUD (visibility meter) and detection feedback (alert states).</li>
  <li>Checkpoint/Fail states and lightweight save of player attempts.</li>
  <li>Packaging settings and a Windows build artifact for quick review.</li>
</ul>

<hr>

<h2 id="about-developer">About the Developer</h2>
<p><b>Rebecca St. Clair</b><br>
🎓 <i>Computer Science Student | Aspiring Software Engineer | Writer</i><br>
<p><i>“Bringing imagination and engineering together — one line of code at a time.”</i></p>

<p>Self-starter and detail-oriented software engineer in training, passionate about combining creativity and logic to design systems that are both functional and meaningful. I learn by doing — building each project piece by piece, debugging relentlessly, and improving through curiosity and persistence. My focus is on writing clean, approachable code, developing maintainable systems, and transforming complex ideas into clear, user-centered experiences that make technology feel transparent and empowering.</p>

<p>
  <a href="https://github.com/RebeccaStClairProjects"><img src="https://img.shields.io/badge/Portfolio-RebeccaStClairProjects-blue" alt="Portfolio Badge"></a><br>
  <a href="https://www.linkedin.com/in/rebecca-st-clair-553225236/"><img src="https://img.shields.io/badge/LinkedIn-Rebecca%20St.%20Clair-blue?logo=linkedin" alt="LinkedIn Badge"></a>
</p>

<hr>

<h2 id="license">License</h2>
<p>MIT License. See the <code>LICENSE</code> file for details.</p>
