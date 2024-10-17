<div class="Box-sc-g0xbh4-0 QkQOb js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><div class="markdown-heading" dir="auto"><h1 tabindex="-1" class="heading-element" dir="auto" _msttexthash="47879182" _msthash="257">用于教育的 QtRvSim–RISC-V CPU 模拟器</h1><a id="user-content-qtrvsimrisc-v-cpu-simulator-for-education" class="anchor" aria-label="永久链接：用于教育的 QtRvSim–RISC-V CPU 模拟器" href="#qtrvsimrisc-v-cpu-simulator-for-education" _mstaria-label="4441450" _msthash="258"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="/cvut/qtrvsim/blob/master/data/screenshots/intro.webp"><img src="/cvut/qtrvsim/raw/master/data/screenshots/intro.webp" alt="QtRvSim 截图" style="max-width: 100%;" _mstalt="352833" _msthash="259"></a></p>
<p dir="auto" _msttexthash="167695580" _msthash="260">由 <a href="http://comparch.edu.cvut.cz" rel="nofollow" _istranslated="1">Computer Architectures Education</a> 项目开发
在<a href="http://www.cvut.cz/" rel="nofollow" _istranslated="1">捷克技术大学</a>。</p>
<p dir="auto" _msttexthash="172521297" _msthash="261"><strong _istranslated="1">您的组织是否在使用 QtRvSim？</strong> <a href="https://github.com/cvut/qtrvsim/discussions/136" data-hovercard-type="discussion" data-hovercard-url="/cvut/qtrvsim/discussions/136/hovercard" _istranslated="1">请在讨论中告诉我们！</a></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto" _msttexthash="5308706" _msthash="262">目录</h2><a id="user-content-table-of-contents" class="anchor" aria-label="永久链接：目录" href="#table-of-contents" _mstaria-label="644748" _msthash="263"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>

<ul dir="auto">
<li><a href="#try-it-out-webassembly" _msttexthash="48140729" _msthash="264">试试看！（WebAssembly）</a></li>
<li><a href="#build-and-packages" _msttexthash="10634507" _msthash="265">生成和包</a>
<ul dir="auto">
<li><a href="#build-dependencies" _msttexthash="17610112" _msthash="266">构建依赖项</a></li>
<li><a href="#general-compilation" _msttexthash="13742352" _msthash="267">一般编译</a></li>
<li><a href="#building-from-source-on-macos" _msttexthash="25542816" _msthash="268">在 macOS 上从源构建</a></li>
<li><a href="#download-binary-packages" _msttexthash="19103513" _msthash="269">下载二进制包</a></li>
<li><a href="#nix-package" _msttexthash="8100807" _msthash="270">Nix 封装</a></li>
<li><a href="#tests" _msttexthash="6268977" _msthash="271">测试</a></li>
</ul>
</li>
<li><a href="#documentation" _msttexthash="5144373" _msthash="272">文档</a></li>
<li><a href="#accepted-binary-formats" _msttexthash="28205294" _msthash="273">接受的二进制格式</a>
<ul dir="auto">
<li><a href="#llvm-toolchain-usage" _msttexthash="22723883" _msthash="274">LLVM 工具链使用</a></li>
<li><a href="#gnu-toolchain-usage" _msttexthash="20979608" _msthash="275">GNU 工具链使用</a></li>
<li><a href="#gnu-64-bit-toolchain-use-for-rv32i-target" _msttexthash="53893086" _msthash="276">用于 RV32I 目标的 GNU 64 位工具链</a></li>
</ul>
</li>
<li><a href="#integrated-assembler" _msttexthash="16758937" _msthash="277">集成汇编器</a></li>
<li><a href="#support-to-call-external-make-utility" _msttexthash="48424129" _msthash="278">支持调用外部 make 实用程序</a></li>
<li><a href="#advanced-functionalities" _msttexthash="13746629" _msthash="279">高级功能</a>
<ul dir="auto">
<li><a href="#peripherals" _msttexthash="5795842" _msthash="280">外设</a></li>
<li><a href="#interrupts-and-control-and-status-registers" _msttexthash="39437684" _msthash="281">中断、控制和状态寄存器</a></li>
<li><a href="#system-calls-support" _msttexthash="22039901" _msthash="282">系统调用支持</a></li>
</ul>
</li>
<li><a href="#limitations-of-the-implementation" _msttexthash="16404752" _msthash="283">实施的限制</a>
<ul dir="auto">
<li><a href="#qtrvsim-limitations" _msttexthash="11198369" _msthash="284">QtRvSim 限制</a></li>
<li><a href="#list-of-currently-supported-instructions" _msttexthash="33077980" _msthash="285">当前支持的指令列表</a></li>
</ul>
</li>
<li><a href="#links-to-resources-and-similar-projects" _msttexthash="45310174" _msthash="286">资源和类似项目的链接</a></li>
<li><a href="#copyright" _msttexthash="5411536" _msthash="287">版权</a></li>
<li><a href="#license" _msttexthash="9675445" _msthash="288">许可证</a></li>
</ul>

<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto" _msttexthash="48140729" _msthash="289">试试看！（WebAssembly）</h2><a id="user-content-try-it-out-webassembly" class="anchor" aria-label="永久链接： 试试看！（WebAssembly）" href="#try-it-out-webassembly" _mstaria-label="896844" _msthash="290"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto" _msttexthash="439739677" _msthash="291">QtRVSim 是可用于 <a href="https://webassembly.org/" rel="nofollow" _istranslated="1">WebAssembly</a> 的实验性功能，它可以在大多数浏览器中运行
无需安装。<strong _istranslated="1"><a href="https://comparch.edu.cvut.cz/qtrvsim/app" rel="nofollow" _istranslated="1">QtRVSim 在线</a></strong></p>
<p dir="auto" _msttexthash="263489265" _msthash="292"><strong _istranslated="1">请注意，WebAssembly 版本是实验性的。</strong>请通过 <a href="https://github.com/cvut/qtrvsim/issues/new" _istranslated="1">GitHub 问题</a>报告任何困难。</p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto" _msttexthash="10634507" _msthash="293">生成和包</h2><a id="user-content-build-and-packages" class="anchor" aria-label="永久链接： Build and packages" href="#build-and-packages" _mstaria-label="669981" _msthash="294"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a href="https://repology.org/project/qtrvsim/versions" rel="nofollow"><img src="https://camo.githubusercontent.com/3aab4d99ebf9fa306daa0911fc41da9ba361a38f436fee4deeef45aaef14749c/68747470733a2f2f7265706f6c6f67792e6f72672f62616467652f766572746963616c2d616c6c7265706f732f7174727673696d2e737667" alt="包装状态" data-canonical-src="https://repology.org/badge/vertical-allrepos/qtrvsim.svg" style="max-width: 100%;" _mstalt="293371" _msthash="295"></a></p>
<p dir="auto"><a href="https://build.opensuse.org/package/show/home:jdupak/qtrvsim" rel="nofollow"><img src="https://camo.githubusercontent.com/1b491ded0926d9b18c424c31dfb2fb21bfcd372fdba0901251795f2058666b00/68747470733a2f2f6275696c642e6f70656e737573652e6f72672f70726f6a656374732f686f6d653a6a647570616b2f7061636b616765732f7174727673696d2f62616467652e7376673f747970653d64656661756c74" alt="构建结果" data-canonical-src="https://build.opensuse.org/projects/home:jdupak/packages/qtrvsim/badge.svg?type=default" style="max-width: 100%;" _mstalt="188409" _msthash="296"></a></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="17610112" _msthash="297">构建依赖项</h3><a id="user-content-build-dependencies" class="anchor" aria-label="永久链接：构建依赖项" href="#build-dependencies" _mstaria-label="710190" _msthash="298"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li _msttexthash="159101618" _msthash="299">Qt 5 （最低测试版本为 5.9.5），对 Qt 6 的实验性支持</li>
<li _msttexthash="206360271" _msthash="300">elfutils （可选;libelf 也可以，但可能会有一些问题）</li>
</ul>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="34647964" _msthash="301">Linux 上的快速编译</h3><a id="user-content-quick-compilation-on-linux" class="anchor" aria-label="永久链接：Linux 上的快速编译" href="#quick-compilation-on-linux" _mstaria-label="1031017" _msthash="302"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="883363000" _msthash="303">在 Linux 上，您可以使用包装器 Makefile 并在项目根目录中运行。它将创建一个构建目录
并在其中运行 CMake。可用目标包括：（默认）和 .</font><code>make</code><code>release</code><code>debug</code></p>
<p dir="auto" _msttexthash="407974775" _msthash="304">打包者注意事项：创建源存档时，CMake 会删除此 Makefile，以避免任何歧义。包
应该直接调用 CMake。</p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="13742352" _msthash="305">一般编译</h3><a id="user-content-general-compilation" class="anchor" aria-label="永久链接： General Compilation" href="#general-compilation" _mstaria-label="767182" _msthash="306"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>cmake -DCMAKE_BUILD_TYPE=Release /path/to/qtrvsim
make</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cmake -DCMAKE_BUILD_TYPE=Release /path/to/qtrvsim
make" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="378043172" _msthash="307">其中 是此项目根目录的路径。构建的二进制文件可以在
build 目录（调用 cmake 的那个目录）。</font><code>/path/to/qtrvsim</code><code>target</code></p>
<p dir="auto"><code>-DCMAKE_BUILD_TYPE=Debug</code><font _mstmutation="1" _msttexthash="53795053" _msthash="308">构建包含排错剂的开发版本。</font></p>
<p dir="auto"><font _mstmutation="1" _msttexthash="83955027" _msthash="309">如果未提供构建类型，则为默认值。</font><code>Debug</code></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="25542816" _msthash="310">在 macOS 上从源构建</h3><a id="user-content-building-from-source-on-macos" class="anchor" aria-label="永久链接：在 macOS 上从源码构建" href="#building-from-source-on-macos" _mstaria-label="1121536" _msthash="311"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="1768353834" _msthash="312">从 App Store 安装最新版本的 <strong _mstmutation="1" _istranslated="1">Xcode</strong>。然后打开一个终端并执行
安装 Command Line Tools。然后打开 Xcode，接受许可协议并等待它安装任何其他
组件。在您最终看到 “Welcome to Xcode” 屏幕后，从顶部栏
选择并选择 SDK 版本。</font><code>xcode-select --install</code><code>Xcode -&gt; Preferences -&gt; Locations -&gt; Command Line Tools</code></p>
<p dir="auto" _msttexthash="246517557" _msthash="313">安装 <a href="https://brew.sh/" rel="nofollow" _istranslated="1">Homebrew</a> 并使用它来安装 Qt。（macOS 版本必须使用捆绑的 libelf）</p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>brew install qt</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="brew install qt" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto" _msttexthash="166624484" _msthash="314">现在，以与一般编译（<a href="#general-compilation" _istranslated="1">上述</a>）相同的方式构建项目。</p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="19103513" _msthash="315">下载二进制包</h3><a id="user-content-download-binary-packages" class="anchor" aria-label="永久链接：下载二进制包" href="#download-binary-packages" _mstaria-label="948246" _msthash="316"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><a href="https://github.com/cvut/qtrvsim/releases" _msttexthash="1383655" _msthash="317">https://github.com/cvut/qtrvsim/releases</a>
<ul dir="auto">
<li _msttexthash="110243159" _msthash="318">带有 Windows 和通用 GNU/Linux 二进制文件的档案</li>
</ul>
</li>
<li><a href="https://build.opensuse.org/repositories/home:jdupak/qtrvsim" rel="nofollow" _msttexthash="2807259" _msthash="319">https://build.opensuse.org/repositories/home:jdupak/qtrvsim</a></li>
<li><a href="https://software.opensuse.org/download.html?project=home%3Ajdupak&amp;package=qtrvsim" rel="nofollow" _msttexthash="4881968" _msthash="320">https://software.opensuse.org/download.html?project=home%3Ajdupak&amp;package=qtrvsim</a>
<ul dir="auto">
<li _msttexthash="31833945" _msthash="321">Open Build Service 二进制包</li>
</ul>
</li>
<li><a href="https://launchpad.net/~qtrvsimteam/+archive/ubuntu/ppa" rel="nofollow" _msttexthash="2335138" _msthash="322">https://launchpad.net/~qtrvsimteam/+archive/ubuntu/ppa</a>
<ul dir="auto">
<li _msttexthash="10891166" _msthash="323">Ubuntu PPA 存档</li>
</ul>
</li>
</ul>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>sudo add-apt-repository ppa:qtrvsimteam/ppa
sudo apt-get update
sudo apt-get install qtrvsim</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="sudo add-apt-repository ppa:qtrvsimteam/ppa
sudo apt-get update
sudo apt-get install qtrvsim" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="8100807" _msthash="324">Nix 封装</h3><a id="user-content-nix-package" class="anchor" aria-label="永久链接：Nix 包" href="#nix-package" _mstaria-label="431938" _msthash="325"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto" _msttexthash="787915440" _msthash="326">QtRVSim 提供了一个 Nix 包作为存储库的一部分。您可以通过以下命令构建和安装它。更新
必须通过签出 git 来手动完成。NIXPKGS 软件包处于 PR 阶段。</p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>nix-env -if <span class="pl-c1">.</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="nix-env -if ." tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="6268977" _msthash="327">测试</h3><a id="user-content-tests" class="anchor" aria-label="永久链接： 测试" href="#tests" _mstaria-label="278863" _msthash="328"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto" _msttexthash="397064317" _msthash="329">测试由 CTest（CMake 的一部分）管理。要构建并运行所有测试，请使用以下命令：</p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>cmake -DCMAKE_BUILD_TYPE=Release /path/to/QtRVSim
make
ctest</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cmake -DCMAKE_BUILD_TYPE=Release /path/to/QtRVSim
make
ctest" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto" _msttexthash="5144373" _msthash="330">文档</h2><a id="user-content-documentation" class="anchor" aria-label="永久链接： 文档" href="#documentation" _mstaria-label="559767" _msthash="331"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto" _msttexthash="112887736" _msthash="332">主要文档在本 README 以及子目录 <a href="/cvut/qtrvsim/blob/master/docs/user" _istranslated="1"><code _istranslated="1">docs/user</code></a> 和 <a href="/cvut/qtrvsim/blob/master/docs/developer" _istranslated="1"><code _istranslated="1">docs/developer</code></a> 中提供。</p>
<p dir="auto" _msttexthash="628864639" _msthash="333">该项目作为 Karel Kočí、Jakub Dupak 和 Max Hollmann 的论文进行开发和扩展。有关链接和参考资料，请参阅 <a href="#resources-and-publications" _istranslated="1">Resources and Publications</a> 部分。</p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto" _msttexthash="28205294" _msthash="334">接受的二进制格式</h2><a id="user-content-accepted-binary-formats" class="anchor" aria-label="永久链接：接受的二进制格式" href="#accepted-binary-formats" _mstaria-label="906334" _msthash="335"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="774317648" _msthash="336">模拟器接受为 RISC-V 目标 （） 编译的 ELF 静态链接可执行文件。
模拟器将根据 ELF 文件头自动选择字节序。
仿真将根据 ELF 文件头以 XLEN=32 或 XLEN=32 执行。</font><code>--march=rv64g</code></p>
<ul dir="auto">
<li _msttexthash="100946651" _msthash="337">支持 64 位 RISC-V ISA RV64IM 和 32 位 RV32IM ELF 可执行文件。</li>
<li _msttexthash="29042273" _msthash="338">尚不支持压缩指令。</li>
</ul>
<p dir="auto"><font _mstmutation="1" _msttexthash="1134996304" _msthash="339">您可以使用专门的 RISC-V GCC/Binutils 工具链 （） 或使用
将 Clang/LLVM 工具链与 <a href="https://lld.llvm.org/" rel="nofollow" _mstmutation="1" _istranslated="1">LLD</a> 统一。如果您已安装 Clang，则不需要任何
其他工具。Clang 可以在 Linux、Windows、macOS 和其他平台上使用......</font><code>riscv32-elf</code></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="22723883" _msthash="340">LLVM 工具链使用</h3><a id="user-content-llvm-toolchain-usage" class="anchor" aria-label="永久链接：LLVM 工具链使用" href="#llvm-toolchain-usage" _mstaria-label="755066" _msthash="341"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>clang --target=riscv32 -march=rv32g -nostdlib -static -fuse-ld=lld test.S -o <span class="pl-c1">test</span>
llvm-objdump -S <span class="pl-c1">test</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="clang --target=riscv32 -march=rv32g -nostdlib -static -fuse-ld=lld test.S -o test
llvm-objdump -S test" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="20979608" _msthash="342">GNU 工具链使用</h3><a id="user-content-gnu-toolchain-usage" class="anchor" aria-label="永久链接：GNU 工具链使用" href="#gnu-toolchain-usage" _mstaria-label="714740" _msthash="343"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>riscv32-elf-as test.S -o test.o
riscv32-elf-ld test.o -o <span class="pl-c1">test</span>
riscv32-elf-objdump -S <span class="pl-c1">test</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="riscv32-elf-as test.S -o test.o
riscv32-elf-ld test.o -o test
riscv32-elf-objdump -S test" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto" _msttexthash="2285010" _msthash="344">或</p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>riscv32-elf-gcc test.S -o <span class="pl-c1">test</span>
riscv32-elf-objdump -S <span class="pl-c1">test</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="riscv32-elf-gcc test.S -o test
riscv32-elf-objdump -S test" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="53893086" _msthash="345">用于 RV32I 目标的 GNU 64 位工具链</h3><a id="user-content-gnu-64-bit-toolchain-use-for-rv32i-target" class="anchor" aria-label="永久链接：用于 RV32I 目标的 GNU 64 位工具链" href="#gnu-64-bit-toolchain-use-for-rv32i-target" _mstaria-label="1636336" _msthash="346"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto" _msttexthash="147011826" _msthash="347">支持 64 位嵌入式工具链的 Multilib 可用于构建可执行文件</p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>riscv64-unknown-elf-gcc -march=rv32i -mabi=ilp32 -nostdlib -o <span class="pl-c1">test</span> test.c crt0local.S -lgcc</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="riscv64-unknown-elf-gcc -march=rv32i -mabi=ilp32 -nostdlib -o test test.c crt0local.S -lgcc" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="363253176" _msthash="348">必须设置全局指针和堆栈才能设置符合运行时 C 代码的环境。当没有其他 C 库
used 然后 next simple 可以使用 。</font><code>crt0local.S</code></p>
<details>
  <summary _msttexthash="11298391" _msthash="349">示例代码</summary>
<div class="highlight highlight-source-assembly notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-en">/</span><span class="pl-s1">*</span><span class="pl-en"> minimal replacement of crt0.o which is else provided by C library </span><span class="pl-s1">*</span><span class="pl-en">/</span>

<span class="pl-en">.globl main</span>
<span class="pl-en">.globl _start</span>
<span class="pl-en">.globl __start</span>

<span class="pl-en">.option norelax</span>

<span class="pl-en">.text</span>

<span class="pl-en">__start:</span>
<span class="pl-en">_start:</span>
<span class="pl-en">        .option </span><span class="pl-k">push</span>
<span class="pl-en">        .option norelax</span>
<span class="pl-en">        la gp</span><span class="pl-s1">,</span><span class="pl-en"> __global_pointer$</span>
<span class="pl-en">        .option </span><span class="pl-k">pop</span>
<span class="pl-en">        la      </span><span class="pl-v">sp</span><span class="pl-s1">,</span><span class="pl-en"> __stack_end</span>
<span class="pl-en">        addi    a0</span><span class="pl-s1">,</span><span class="pl-en"> zero</span><span class="pl-s1">,</span><span class="pl-en"> </span><span class="pl-c1">0</span>
<span class="pl-en">        addi    a1</span><span class="pl-s1">,</span><span class="pl-en"> zero</span><span class="pl-s1">,</span><span class="pl-en"> </span><span class="pl-c1">0</span>
<span class="pl-en">        jal     main</span>
<span class="pl-en">quit:</span>
<span class="pl-en">        addi    a0</span><span class="pl-s1">,</span><span class="pl-en"> zero</span><span class="pl-s1">,</span><span class="pl-en"> </span><span class="pl-c1">0</span>
<span class="pl-en">        addi    a7</span><span class="pl-s1">,</span><span class="pl-en"> zero</span><span class="pl-s1">,</span><span class="pl-en"> </span><span class="pl-c1">93</span><span class="pl-en">  /</span><span class="pl-s1">*</span><span class="pl-en"> SYS_exit </span><span class="pl-s1">*</span><span class="pl-en">/</span>
<span class="pl-en">        ecall</span>

<span class="pl-k">loop</span><span class="pl-en">:   ebreak</span>
<span class="pl-en">        beq     zero</span><span class="pl-s1">,</span><span class="pl-en"> zero</span><span class="pl-s1">,</span><span class="pl-en"> </span><span class="pl-k">loop</span>

<span class="pl-en">.bss</span>

<span class="pl-en">__stack_start:</span>
<span class="pl-en">        .skip   </span><span class="pl-c1">4096</span>
<span class="pl-en">__stack_end:</span>

<span class="pl-en">.end _start</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="/* minimal replacement of crt0.o which is else provided by C library */

.globl main
.globl _start
.globl __start

.option norelax

.text

__start:
_start:
        .option push
        .option norelax
        la gp, __global_pointer$
        .option pop
        la      sp, __stack_end
        addi    a0, zero, 0
        addi    a1, zero, 0
        jal     main
quit:
        addi    a0, zero, 0
        addi    a7, zero, 93  /* SYS_exit */
        ecall

loop:   ebreak
        beq     zero, zero, loop

.bss

__stack_start:
        .skip   4096
__stack_end:

.end _start" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</details>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto" _msttexthash="16758937" _msthash="350">集成汇编器</h2><a id="user-content-integrated-assembler" class="anchor" aria-label="永久链接：集成汇编器" href="#integrated-assembler" _mstaria-label="810992" _msthash="351"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="2658189625" _msthash="352">基本集成汇编器包含在模拟器中。<a href="https://sourceware.org/binutils/docs/as/" rel="nofollow" _mstmutation="1" _istranslated="1">GNU 汇编器</a>指令的一小部分也被认可。next 指令是
已识别：、 、 / 和 .其他一些指令被简单地忽略：、、 、 和 .
这允许编写可由集成和全功能汇编器编译的代码。地址已分配
到存储在 Symbol Table 中的标签/符号。加法、减法、乘法、除法和按位 AND 或
认可。</font><code>.word</code><code>.orig</code><code>.set</code><code>.equ</code><code>.ascii</code><code>.asciz</code><code>.data</code><code>.text</code><code>.globl</code><code>.end</code><code>.ent</code></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto" _msttexthash="48424129" _msthash="353">支持调用外部 make 实用程序</h2><a id="user-content-support-to-call-external-make-utility" class="anchor" aria-label="永久链接：支持调用外部 make 工具" href="#support-to-call-external-make-utility" _mstaria-label="1617356" _msthash="354"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto" _msttexthash="4945071144" _msthash="355">操作 “Build executable by external make” 调用 “make” 程序。如果调用了该操作，并且某些源代码编辑器
在主 Windows 选项卡中选择，则 “make” 将在相应的目录中启动。上次选择的 Else 目录
editor 被选中。如果未打开编辑器，则最后加载的 ELF 可执行文件的目录将用作“make”启动路径。如果
即使这不是一个选项，则使用模拟器启动时的默认目录。</p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto" _msttexthash="13746629" _msthash="356">高级功能</h2><a id="user-content-advanced-functionalities" class="anchor" aria-label="永久链接：高级功能" href="#advanced-functionalities" _mstaria-label="1031212" _msthash="357"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="5795842" _msthash="358">外设</h3><a id="user-content-peripherals" class="anchor" aria-label="永久链接： 外围设备" href="#peripherals" _mstaria-label="477958" _msthash="359"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<details>
  <summary _msttexthash="93088047" _msthash="360">模拟 LCD、旋钮、按钮、串行端口、定时器...</summary>
<p dir="auto" _msttexthash="87078849" _msthash="361">模拟器目前实现了两个外围设备的仿真。</p>
<p dir="auto"><font _mstmutation="1" _msttexthash="10066735588" _msthash="362">第一个是简单串行端口 （UART）。它支持传输
（Tx） 和接收 （Rx）。接收器状态寄存器 （）
实现两个位。只读位 0 （）
如果接收器数据寄存器 （） 中有未读字符可用，则设置为 1。位 1
（） 可以写入 1 以在未读字符可用时启用中断请求。这
发射机状态寄存器 （） 位 0
（SERP_TX_ST_REG_READY） 通过值 1 发出信号，表明 UART 已准备就绪，可以接受要发送的下一个字符。位 1
（） 启用中断的生成。寄存器是实际的 Tx 缓冲区。LSB 字节
的文字被传输到终端窗口。外设基址和寄存器的定义
offsets （） 和单个字段 masks （） 紧随其后</font><code>SERP_RX_ST_REG</code><code>SERP_RX_ST_REG_READY</code><code>SERP_RX_DATA_REG</code><code>SERP_RX_ST_REG_IE</code><code>SERP_TX_ST_REG</code><code>SERP_TX_ST_REG_IE</code><code>SERP_TX_DATA_REG</code><code>_o</code><code>_m</code></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>#define SERIAL_PORT_BASE   0xffffc000

#define SERP_RX_ST_REG_o           0x00
#define SERP_RX_ST_REG_READY_m      0x1
#define SERP_RX_ST_REG_IE_m         0x2

#define SERP_RX_DATA_REG_o         0x04

#define SERP_TX_ST_REG_o           0x08
#define SERP_TX_ST_REG_READY_m      0x1
#define SERP_TX_ST_REG_IE_m         0x2

#define SERP_TX_DATA_REG_o         0x0c
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="#define SERIAL_PORT_BASE   0xffffc000

#define SERP_RX_ST_REG_o           0x00
#define SERP_RX_ST_REG_READY_m      0x1
#define SERP_RX_ST_REG_IE_m         0x2

#define SERP_RX_DATA_REG_o         0x04

#define SERP_TX_ST_REG_o           0x08
#define SERP_TX_ST_REG_READY_m      0x1
#define SERP_TX_ST_REG_IE_m         0x2

#define SERP_TX_DATA_REG_o         0x0c" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto" _msttexthash="329703647" _msthash="363">UART 寄存器区域镜像在地址0xffff0000上，以便使用最初编写的程序
用于 <a href="http://spimsimulator.sourceforge.net/" rel="nofollow" _istranslated="1">SPIM</a> 或 <a href="http://courses.missouristate.edu/KenVollmar/MARS/" rel="nofollow" _istranslated="1">MARS</a> 仿真器。</p>
<p dir="auto"><font _mstmutation="1" _msttexthash="1950811863" _msthash="364">另一个外设允许设置连接到单个字（只读寄存器）的三个字节值
从由旋钮设置的用户面板，以十六进制、十进制和二进制格式（寄存器）显示一个字。那里
是另外两个可写的单词，用于控制 RGB LED 1 和 2 的颜色
（寄存器和 ）。</font><code>KNOBS_8BIT</code><code>LED_LINE</code><code>LED_RGB1</code><code>LED_RGB2</code></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>#define SPILED_REG_BASE    0xffffc100

#define SPILED_REG_LED_LINE_o           0x004
#define SPILED_REG_LED_RGB1_o           0x010
#define SPILED_REG_LED_RGB2_o           0x014
#define SPILED_REG_LED_KBDWR_DIRECT_o   0x018

#define SPILED_REG_KBDRD_KNOBS_DIRECT_o 0x020
#define SPILED_REG_KNOBS_8BIT_o         0x024
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="#define SPILED_REG_BASE    0xffffc100

#define SPILED_REG_LED_LINE_o           0x004
#define SPILED_REG_LED_RGB1_o           0x010
#define SPILED_REG_LED_RGB2_o           0x014
#define SPILED_REG_LED_KBDWR_DIRECT_o   0x018

#define SPILED_REG_KBDRD_KNOBS_DIRECT_o 0x020
#define SPILED_REG_KNOBS_8BIT_o         0x024" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="1606532772" _msthash="365">实现了简单的每像素 16 位 （RGB565） 帧缓冲和 LCD。framebuffer 映射到 range starting
at 地址。显示尺寸为 480 x 320 像素。像素格式 RGB565 预期红色分量位为 11..
15，绿色分量在第 5..10 位，蓝色分量在第 0..4 位。</font><code>LCD_FB_START</code></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>#define LCD_FB_START       0xffe00000
#define LCD_FB_END         0xffe4afff
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="#define LCD_FB_START       0xffe00000
#define LCD_FB_END         0xffe4afff" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto" _msttexthash="141690341" _msthash="366">RISC-V Advanced Core 本地中断器的基本实现
通过对</p>
<ul dir="auto">
<li _msttexthash="70945251" _msthash="367">计算机级计时器设备 （MTIMER）</li>
<li _msttexthash="66119560" _msthash="368">机器级软件中断设备 （MSWI）</li>
</ul>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>#define ACLINT_MSWI        0xfffd0000 // core 0 machine SW interrupt request
#define ACLINT_MTIMECMP    0xfffd4000 // core 0 compare value
#define ACLINT_MTIME       0xfffdbff8 // timer base 10 MHz
#define ACLINT_SSWI        0xfffd0000 // core 0 system SW interrupt request
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="#define ACLINT_MSWI        0xfffd0000 // core 0 machine SW interrupt request
#define ACLINT_MTIMECMP    0xfffd4000 // core 0 compare value
#define ACLINT_MTIME       0xfffdbff8 // timer base 10 MHz
#define ACLINT_SSWI        0xfffd0000 // core 0 system SW interrupt request" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto" _msttexthash="221648973" _msthash="369">有关 ACLINT 的更多信息，请参阅 <a href="https://github.com/riscv/riscv-aclint/blob/main/riscv-aclint.adoc" _istranslated="1">RISC-V 高级内核本地中断器规范</a>。</p>
</details>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="39437684" _msthash="370">中断、控制和状态寄存器</h3><a id="user-content-interrupts-and-control-and-status-registers" class="anchor" aria-label="永久链接： 中断和控制以及状态寄存器" href="#interrupts-and-control-and-status-registers" _mstaria-label="2013128" _msthash="371"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<details>
  <summary _msttexthash="42206073" _msthash="372">实施的 CSR 寄存器及其使用</summary>
<p dir="auto" _msttexthash="25753013" _msthash="373">中断源列表：</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th align="right" _msttexthash="7334925" _msthash="374">Irq 编号</th>
<th align="right" _msttexthash="10828064" _msthash="375">mie / mip 比特</th>
<th align="left" _msttexthash="2575664" _msthash="376">源</th>
</tr>
</thead>
<tbody>
<tr>
<td align="right" _msttexthash="4641" _msthash="377">3</td>
<td align="right" _msttexthash="4641" _msthash="378">3</td>
<td align="left" _msttexthash="29650959" _msthash="379">机器软件中断请求</td>
</tr>
<tr>
<td align="right" _msttexthash="5005" _msthash="380">7</td>
<td align="right" _msttexthash="5005" _msthash="381">7</td>
<td align="left" _msttexthash="21526245" _msthash="382">机器定时器中断</td>
</tr>
<tr>
<td align="right" _msttexthash="10075" _msthash="383">16</td>
<td align="right" _msttexthash="10075" _msthash="384">16</td>
<td align="left" _msttexthash="39082940" _msthash="385">有接收的字符可供读取</td>
</tr>
<tr>
<td align="right" _msttexthash="10179" _msthash="386">17</td>
<td align="right" _msttexthash="10179" _msthash="387">17</td>
<td align="left" _msttexthash="58315595" _msthash="388">串行端口已准备好接受 Tx 的字符</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
<p dir="auto" _msttexthash="37249706" _msthash="389">可识别以下 Control Status 寄存器</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th align="right" _msttexthash="2363088" _msthash="390">数</th>
<th align="left" _msttexthash="4389879" _msthash="391">名字</th>
<th align="left" _msttexthash="6157333" _msthash="392">描述</th>
</tr>
</thead>
<tbody>
<tr>
<td align="right" _msttexthash="35919" _msthash="393">0x300</td>
<td align="left" _msttexthash="102336" _msthash="394">mstatus</td>
<td align="left" _msttexthash="24318398" _msthash="395">机器状态寄存器。</td>
</tr>
<tr>
<td align="right" _msttexthash="36491" _msthash="396">0x304</td>
<td align="left" _msttexthash="5699707" _msthash="397">三重</td>
<td align="left" _msttexthash="33286838" _msthash="398">机器中断启用寄存器。</td>
</tr>
<tr>
<td align="right" _msttexthash="36634" _msthash="399">0x305</td>
<td align="left" _msttexthash="63076" _msthash="400">mtvec</td>
<td align="left" _msttexthash="20326566" _msthash="401">Machine trap-handler 基址。</td>
</tr>
<tr>
<td align="right" _msttexthash="36439" _msthash="402">0x340</td>
<td align="left" _msttexthash="6032208" _msthash="403">mscratch 的</td>
<td align="left" _msttexthash="68710122" _msthash="404">机器陷阱处理程序的暂存寄存器。</td>
</tr>
<tr>
<td align="right" _msttexthash="36582" _msthash="405">0x341</td>
<td align="left" _msttexthash="32253" _msthash="406">MEPC</td>
<td align="left" _msttexthash="44097404" _msthash="407">计算机异常程序计数器。</td>
</tr>
<tr>
<td align="right" _msttexthash="36725" _msthash="408">0x342</td>
<td align="left" _msttexthash="4106544" _msthash="409">因为</td>
<td align="left" _msttexthash="22817990" _msthash="410">机器陷阱原因。</td>
</tr>
<tr>
<td align="right" _msttexthash="36868" _msthash="411">0x343</td>
<td align="left" _msttexthash="45123" _msthash="412">MTVAL</td>
<td align="left" _msttexthash="37667539" _msthash="413">机器地址或指令错误。</td>
</tr>
<tr>
<td align="right" _msttexthash="37011" _msthash="414">0x344</td>
<td align="left" _msttexthash="23959" _msthash="415">MIP</td>
<td align="left" _msttexthash="28270021" _msthash="416">计算机中断挂起。</td>
</tr>
<tr>
<td align="right" _msttexthash="38870" _msthash="417">0x34A</td>
<td align="left" _msttexthash="82797" _msthash="418">mtinsr</td>
<td align="left" _msttexthash="59959484" _msthash="419">机器陷阱指令 （转换）。</td>
</tr>
<tr>
<td align="right" _msttexthash="39013" _msthash="420">0x34B</td>
<td align="left" _msttexthash="52923" _msthash="421">MTVAL2</td>
<td align="left" _msttexthash="51235717" _msthash="422">机器客户机物理地址错误。</td>
</tr>
<tr>
<td align="right" _msttexthash="37674" _msthash="423">0xB00</td>
<td align="left" _msttexthash="78442" _msthash="424">mcycle</td>
<td align="left" _msttexthash="26558129" _msthash="425">机器循环计数器。</td>
</tr>
<tr>
<td align="right" _msttexthash="37960" _msthash="426">0xB02</td>
<td align="left" _msttexthash="11702652" _msthash="427">吟游诗人</td>
<td align="left" _msttexthash="52288847" _msthash="428">机器说明-已停用的计数器。</td>
</tr>
<tr>
<td align="right" _msttexthash="38415" _msthash="429">0xF11</td>
<td align="left" _msttexthash="137800" _msthash="430">mvendorid</td>
<td align="left" _msttexthash="8863101" _msthash="431">供应商 ID。</td>
</tr>
<tr>
<td align="right" _msttexthash="38558" _msthash="432">0xF12</td>
<td align="left" _msttexthash="11869364" _msthash="433">马尔基德</td>
<td align="left" _msttexthash="6946901" _msthash="434">架构 ID。</td>
</tr>
<tr>
<td align="right" _msttexthash="38701" _msthash="435">0xF13</td>
<td align="left" _msttexthash="8925748" _msthash="436">米皮德</td>
<td align="left" _msttexthash="6989229" _msthash="437">实现 ID。</td>
</tr>
<tr>
<td align="right" _msttexthash="38844" _msthash="438">0xF14</td>
<td align="left" _msttexthash="5806632" _msthash="439">哈迪</td>
<td align="left" _msttexthash="14863550" _msthash="440">硬件线程 ID。</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
<p dir="auto"><code>csrr</code><font _mstmutation="1" _msttexthash="123851728" _msthash="441">、 、 、 和 用于从 RISC-V 控制状态寄存器复制和交换值。</font><code>csrw</code><code>csrrs</code><code>csrrs</code><code>csrrw</code></p>
<p dir="auto" _msttexthash="60690110" _msthash="442">启用串口接收中断的顺序：</p>
<p dir="auto"><font _mstmutation="1" _msttexthash="557141559" _msthash="443">首先确定中断服务例程的位置。公共陷阱处理程序的地址由 register 定义，然后在接受异常或中断时将 PC 设置为此地址。</font><code>mtvec</code></p>
<p dir="auto"><font _mstmutation="1" _msttexthash="661037468" _msthash="444">启用机器 Interrupt-Enable 寄存器 （） 中的第 16 位。确保将机器状态寄存器的第 3 位（ - 机器全局中断启用）设置为 1。</font><code>mie</code><code>mstatus.mie</code></p>
<p dir="auto"><font _mstmutation="1" _msttexthash="127741055" _msthash="445">在接收器状态寄存器中启用中断（的第 1 位）。</font><code>SERP_RX_ST_REG</code></p>
<p dir="auto"><font _mstmutation="1" _msttexthash="900980067" _msthash="446">将 character 写入终端。如果启用了中断，则串行端口接收器应立即使用它
在。CPU 应报告中断异常，并且当它传播到执行阶段时设置为
中断例程 start address。</font><code>SERP_RX_ST_REG</code><code>PC</code></p>
</details>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="22039901" _msthash="447">系统调用支持</h3><a id="user-content-system-calls-support" class="anchor" aria-label="永久链接：系统调用支持" href="#system-calls-support" _mstaria-label="782431" _msthash="448"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<details>
  <summary _msttexthash="21983364" _msthash="449">Syscall 表和文档</summary>
<p dir="auto" _msttexthash="157127295" _msthash="450">该模拟器包括对一些 Linux 内核系统调用的支持。使用了 RV32G ilp32 ABI。</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th align="left" _msttexthash="4708184" _msthash="451">注册</th>
<th align="left" _msttexthash="19273046" _msthash="452">在输入时使用</th>
<th align="left" _msttexthash="19290479" _msthash="453">在输出时使用</th>
<th align="left" _msttexthash="13222755" _msthash="454">调用约定</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left" _msttexthash="19663345" _msthash="455">零 （x0）</td>
<td align="left" _msttexthash="747292" _msthash="456">—</td>
<td align="left">-</td>
<td align="left" _msttexthash="15455947" _msthash="457">硬连线零</td>
</tr>
<tr>
<td align="left" _msttexthash="17860609" _msthash="458">RA （x1）</td>
<td align="left" _msttexthash="747292" _msthash="459">—</td>
<td align="left" _msttexthash="20069855" _msthash="460">（保留）</td>
<td align="left" _msttexthash="12627784" _msthash="461">退货地址</td>
</tr>
<tr>
<td align="left" _msttexthash="17862403" _msthash="462">SP （x2）</td>
<td align="left" _msttexthash="747292" _msthash="463">—</td>
<td align="left" _msttexthash="45590558" _msthash="464">（被调用方已保存）</td>
<td align="left" _msttexthash="12729509" _msthash="465">堆栈指针</td>
</tr>
<tr>
<td align="left" _msttexthash="17861454" _msthash="466">GP （x3）</td>
<td align="left" _msttexthash="747292" _msthash="467">—</td>
<td align="left" _msttexthash="20069855" _msthash="468">（保留）</td>
<td align="left" _msttexthash="12261691" _msthash="469">全局指针</td>
</tr>
<tr>
<td align="left" _msttexthash="27723748" _msthash="470">传送卷 （x4）</td>
<td align="left" _msttexthash="747292" _msthash="471">—</td>
<td align="left" _msttexthash="20069855" _msthash="472">（保留）</td>
<td align="left" _msttexthash="14111136" _msthash="473">线程指针</td>
</tr>
<tr>
<td align="left" _msttexthash="28149108" _msthash="474">t0 ..T2 （x5 .. x7）</td>
<td align="left" _msttexthash="747292" _msthash="475">—</td>
<td align="left">-</td>
<td align="left" _msttexthash="4536428" _msthash="476">临时</td>
</tr>
<tr>
<td align="left" _msttexthash="22985339" _msthash="477">S0/FP （x8）</td>
<td align="left" _msttexthash="747292" _msthash="478">—</td>
<td align="left" _msttexthash="45590558" _msthash="479">（被调用方已保存）</td>
<td align="left" _msttexthash="34937929" _msthash="480">保存的寄存器/帧指针</td>
</tr>
<tr>
<td align="left" _msttexthash="43229628" _msthash="481">S1 四门轿车 （x9）</td>
<td align="left" _msttexthash="747292" _msthash="482">—</td>
<td align="left" _msttexthash="45590558" _msthash="483">（被调用方已保存）</td>
<td align="left" _msttexthash="21740498" _msthash="484">已保存的寄存器</td>
</tr>
<tr>
<td align="left" _msttexthash="44085067" _msthash="485">A0 四门轿车 （x10）</td>
<td align="left" _msttexthash="16158974" _msthash="486">第 1 个 syscall 参数</td>
<td align="left" _msttexthash="8066552" _msthash="487">返回值</td>
<td align="left" _msttexthash="23742368" _msthash="488">函数参数/返回值</td>
</tr>
<tr>
<td align="left" _msttexthash="44085379" _msthash="489">A1 四门轿车 （x11）</td>
<td align="left" _msttexthash="18245110" _msthash="490">第二个 syscall 参数</td>
<td align="left">-</td>
<td align="left" _msttexthash="23742368" _msthash="491">函数参数/返回值</td>
</tr>
<tr>
<td align="left" _msttexthash="29868852" _msthash="492">a2 ..A5 （x12 .. x15）</td>
<td align="left" _msttexthash="9064549" _msthash="493">syscall 参数</td>
<td align="left">-</td>
<td align="left" _msttexthash="10495225" _msthash="494">函数参数</td>
</tr>
<tr>
<td align="left" _msttexthash="44086939" _msthash="495">A6 四门轿车 （x16）</td>
<td align="left">-</td>
<td align="left">-</td>
<td align="left" _msttexthash="10495225" _msthash="496">函数参数</td>
</tr>
<tr>
<td align="left" _msttexthash="44087251" _msthash="497">A7 四门轿车 （x17）</td>
<td align="left" _msttexthash="22387534" _msthash="498">系统调用编号</td>
<td align="left">-</td>
<td align="left" _msttexthash="10495225" _msthash="499">函数参数</td>
</tr>
<tr>
<td align="left" _msttexthash="31584410" _msthash="500">S2 ..S11 （x18 .. x27）</td>
<td align="left" _msttexthash="747292" _msthash="501">—</td>
<td align="left" _msttexthash="45590558" _msthash="502">（被调用方已保存）</td>
<td align="left" _msttexthash="17690803" _msthash="503">保存的寄存器</td>
</tr>
<tr>
<td align="left" _msttexthash="29874429" _msthash="504">t3 ..T6 （x28 .. x31）</td>
<td align="left" _msttexthash="747292" _msthash="505">—</td>
<td align="left">-</td>
<td align="left" _msttexthash="4536428" _msthash="506">临时</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
<p dir="auto" _msttexthash="94654352" _msthash="507">所有系统调用的 input 参数都在 register 中传递。</p>
<p dir="auto" _msttexthash="23103561" _msthash="508">支持的 syscall：</p>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto" _msttexthash="95445857" _msthash="509">无效<a href="http://man7.org/linux/man-pages/man2/exit.2.html" rel="nofollow" _istranslated="1">退出</a> （int 状态） __NR_exit （93）</h4><a id="user-content-void-exitint-status-__nr_exit-93" class="anchor" aria-label="永久链接： void exit（int status） __NR_exit （93）" href="#void-exitint-status-__nr_exit-93" _mstaria-label="1383408" _msthash="510"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto" _msttexthash="240642376" _msthash="511">停止/结束程序的执行。参数是 exit status code，0 表示 OK，其他值通知 error。</p>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto" _msttexthash="199629742" _msthash="512">ssize_t <a href="http://man7.org/linux/man-pages/man2/read.2.html" rel="nofollow" _istranslated="1">read</a>（int fd， void *buf， size_t count） __NR_read （63）</h4><a id="user-content-ssize_t-readint-fd-void-buf-size_t-count-__nr_read-63" class="anchor" aria-label="永久链接： ssize_t read（int fd， void *buf， size_t count） __NR_read （63）" href="#ssize_t-readint-fd-void-buf-size_t-count-__nr_read-63" _mstaria-label="2780635" _msthash="513"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="2233732722" _msthash="514">从打开的文件描述符 中读取字节。仿真器将文件描述符 0、1 和 2 映射到内部
终端/控制台仿真器。无需调用即可使用它们。如果没有更多字符要从
console 中，会附加 newline 来获取。读取的 count 字节最多存储到 argument 指定的内存位置。返回实际读取的字节数。</font><code>count</code><code>fd</code><code>open</code><code>buf</code></p>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto" _msttexthash="223980822" _msthash="515">ssize_t <a href="http://man7.org/linux/man-pages/man2/write.2.html" rel="nofollow" _istranslated="1">write</a>（int fd， const void *buf， size_t count） __NR_write （64）</h4><a id="user-content-ssize_t-writeint-fd-const-void-buf-size_t-count-__nr_write-64" class="anchor" aria-label="永久链接： ssize_t write（int fd， const void *buf， size_t count） __NR_write （64）" href="#ssize_t-writeint-fd-const-void-buf-size_t-count-__nr_write-64" _mstaria-label="3490383" _msthash="516"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="203342243" _msthash="517">将字节从内存位置写入打开的文件描述符 。文件句柄 0、1 和 2 的控制台与 .</font><code>count</code><code>buf</code><code>fd</code><code>read</code></p>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto" _msttexthash="88051041" _msthash="518">int <a href="http://man7.org/linux/man-pages/man2/close.2.html" rel="nofollow" _istranslated="1">close</a>（int fd） __NR_close （57）</h4><a id="user-content-int-closeint-fd-__nr_close-57" class="anchor" aria-label="永久链接： int close（int fd） __NR_close （57）" href="#int-closeint-fd-__nr_close-57" _mstaria-label="1174784" _msthash="519"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="89244532" _msthash="520">关闭与 descriptor 和 release descriptor 关联的文件。</font><code>fd</code></p>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto" _msttexthash="306650370" _msthash="521">int <a href="http://man7.org/linux/man-pages/man2/open.2.html" rel="nofollow" _istranslated="1">openat</a>（int dirfd， const char *pathname， int flags， mode_t mode） __NR_openat （56）</h4><a id="user-content-int-openatint-dirfd-const-char-pathname-int-flags-mode_t-mode-__nr_openat-56" class="anchor" aria-label="永久链接： int openat（int dirfd， const char *pathname， int flags， mode_t mode） __NR_openat （56）" href="#int-openatint-dirfd-const-char-pathname-int-flags-mode_t-mode-__nr_openat-56" _mstaria-label="4902157" _msthash="522"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="3266873636" _msthash="523">打开文件并将其与第一个未使用的文件描述符编号关联，然后返回该编号。如果
选项 -&gt; 不为空，则从模拟环境接收的文件路径将附加到指定的路径
由。主机文件系统受到保护，防止尝试使用 path 元素遍历到随机目录。如果未指定 root，则所有打开的文件都将定向到模拟终端。仅支持 （ = -100） 模式。</font><code>OS Emulation</code><code>Filesystem root</code><code>pathname</code><code>Filesystem root</code><code>..</code><code>TARGET_AT_FDCWD</code><code>dirfd</code></p>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto" _msttexthash="95762888" _msthash="524">void * <a href="http://man7.org/linux/man-pages/man2/brk.2.html" rel="nofollow" _istranslated="1">brk</a>（void *addr） __NR_brk （214）</h4><a id="user-content-void--brkvoid-addr-__nr_brk-214" class="anchor" aria-label="永久链接： void * brk（void *addr） __NR_brk （214）" href="#void--brkvoid-addr-__nr_brk-214" _mstaria-label="1267175" _msthash="525"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto" _msttexthash="601827629" _msthash="526">设置程序 data/bss 结束后标准堆使用的区域的结尾。syscall 由 dummy 模拟
实现。最多 0xffff0000 个地址空间由自动连接的 RAM 备份。</p>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto" _msttexthash="159531450" _msthash="527">int <a href="http://man7.org/linux/man-pages/man2/ftruncate.2.html" rel="nofollow" _istranslated="1">ftruncate</a>（int fd， off_t length） __NR_truncate （46）</h4><a id="user-content-int-ftruncateint-fd-off_t-length-__nr_truncate-46" class="anchor" aria-label="永久链接： int ftruncate（int fd， off_t length） __NR_truncate （46）" href="#int-ftruncateint-fd-off_t-length-__nr_truncate-46" _mstaria-label="2510521" _msthash="528"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="495042405" _msthash="529">将 指定的打开文件的长度设置为新的 .即使在 32 位系统上，参数也是 64 位的，并且它作为
第二个和第三个参数。</font><code>fd</code><code>length</code><code>length</code></p>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto" _msttexthash="243075755" _msthash="530">ssize_t <a href="http://man7.org/linux/man-pages/man2/readv.2.html" rel="nofollow" _istranslated="1">readv</a>（int fd， const struct iovec *iov， int iovcnt） __NR_Linux （65）</h4><a id="user-content-ssize_t-readvint-fd-const-struct-iovec-iov-int-iovcnt-__nr_linux-65" class="anchor" aria-label="永久链接： ssize_t readv（int fd， const struct iovec *iov， int iovcnt） __NR_Linux （65）" href="#ssize_t-readvint-fd-const-struct-iovec-iov-int-iovcnt-__nr_linux-65" _mstaria-label="3992768" _msthash="531"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="382093426" _msthash="532">要读取的数据所在的系统调用的变体将存储到由成对
基址，地址传入时存储在内存中的长度对。</font><code>read</code><code>iovcnt</code><code>iov</code></p>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto" _msttexthash="248264705" _msthash="533">ssize_t <a href="http://man7.org/linux/man-pages/man2/writev.2.html" rel="nofollow" _istranslated="1">writev</a>（int fd， const struct iovec *iov， int iovcnt） __NR_Linux （66）</h4><a id="user-content-ssize_t-writevint-fd-const-struct-iovec-iov-int-iovcnt-__nr_linux-66" class="anchor" aria-label="永久链接： ssize_t writev（int fd， const struct iovec *iov， int iovcnt） __NR_Linux （66）" href="#ssize_t-writevint-fd-const-struct-iovec-iov-int-iovcnt-__nr_linux-66" _mstaria-label="4111094" _msthash="534"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="269374274" _msthash="535">要写入数据的系统调用变体由基址对定义，长度对在地址传入时存储在内存中。</font><code>write</code><code>iovcnt</code><code>iov</code></p>
</details>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto" _msttexthash="16404752" _msthash="536">实施的限制</h2><a id="user-content-limitations-of-the-implementation" class="anchor" aria-label="永久链接： 实现的限制" href="#limitations-of-the-implementation" _mstaria-label="1453036" _msthash="537"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li _msttexthash="58287177" _msthash="538">请参阅当前支持的说明列表。</li>
</ul>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="11198369" _msthash="539">QtRvSim 限制</h3><a id="user-content-qtrvsim-limitations" class="anchor" aria-label="永久链接：QtRvSim 限制" href="#qtrvsim-limitations" _mstaria-label="780026" _msthash="540"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li _msttexthash="124102849" _msthash="541">目前仅实现了对特权指令的极少支持（mret）。</li>
<li _msttexthash="103398958" _msthash="542">仅实施计算机模式和计算机 CSR 的最小子集。</li>
<li _msttexthash="35577347" _msthash="543">未实现 TLB 和虚拟内存。</li>
<li _msttexthash="15245919" _msthash="544">不支持浮点</li>
<li _msttexthash="606065967" _msthash="545">内存访问停顿（由于缓存未命中而导致执行停顿对用户来说非常烦人，因此
缓存和内存只是在收集的统计信息中）</li>
<li><font _mstmutation="1" _msttexthash="770175848" _msthash="546">对中断和异常的有限支持。当识别到指令时，Linux 内核系统的一小部分调用
可以通过 Trap Handler 进行模拟或将模拟器配置为继续
在地址上。</font><code>ecall</code><code>mtvec</code></li>
</ul>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="33077980" _msthash="547">当前支持的指令列表</h3><a id="user-content-list-of-currently-supported-instructions" class="anchor" aria-label="永久链接：当前支持的指令列表" href="#list-of-currently-supported-instructions" _mstaria-label="1889654" _msthash="548"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><font _mstmutation="1" _msttexthash="10227048" _msthash="549"><strong _mstmutation="1" _istranslated="1">RV32I</strong>：</font><ul dir="auto">
<li><font _mstmutation="1" _msttexthash="14748591" _msthash="550"><strong _mstmutation="1" _istranslated="1">负载</strong>：</font><code>lw, lh, lb, lwu, lhu, lbu</code></li>
<li><font _mstmutation="1" _msttexthash="12145692" _msthash="551"><strong _mstmutation="1" _istranslated="1">商店</strong>：</font><code>sw, sh, sb, swu, shu, sbu</code></li>
<li><font _mstmutation="1" _msttexthash="12055069" _msthash="552"><strong _mstmutation="1" _istranslated="1">OP</strong>的：</font><code>add, sub, sll, slt, sltu, xor, srl, sra, or, and</code></li>
<li><font _mstmutation="1" _msttexthash="16681652" _msthash="553"><strong _mstmutation="1" _istranslated="1">杂项 MEM</strong>：</font><code>fence, fence.i</code></li>
<li><font _mstmutation="1" _msttexthash="11090001" _msthash="554"><strong _mstmutation="1" _istranslated="1">OP-IMM</strong>：</font><code>addi, sll, slti, sltiu, xori, srli, srai, ori, andi, auipc, lui</code></li>
<li><font _mstmutation="1" _msttexthash="15083406" _msthash="555"><strong _mstmutation="1" _istranslated="1">分公司</strong>：</font><code>beq, bne, btl, bge, bltu, bgtu</code></li>
<li><font _mstmutation="1" _msttexthash="14721915" _msthash="556"><strong _mstmutation="1" _istranslated="1">跳跃</strong>：</font><code>jal, jalr</code></li>
<li><font _mstmutation="1" _msttexthash="13930163" _msthash="557"><strong _mstmutation="1" _istranslated="1">系统</strong>：</font><code>ecall, mret, ebreak, csrrw, csrrs, csrrc, csrrwi, csrrsi, csrrci</code></li>
</ul>
</li>
<li><font _mstmutation="1" _msttexthash="10227659" _msthash="558"><strong _mstmutation="1" _istranslated="1">RV64I</strong>：</font><ul dir="auto">
<li><font _mstmutation="1" _msttexthash="21930883" _msthash="559"><strong _mstmutation="1" _istranslated="1">加载/存储</strong>：</font><code>lwu, ld, sd</code></li>
<li><font _mstmutation="1" _msttexthash="10222290" _msthash="560"><strong _mstmutation="1" _istranslated="1">OP-32</strong>：</font><code>addw, subw, sllw, srlw, sraw, or, and</code></li>
<li><font _mstmutation="1" _msttexthash="20823270" _msthash="561"><strong _mstmutation="1" _istranslated="1">OP-IMM-32</strong> 的：</font><code>addiw, sllw, srliw, sraiw</code></li>
</ul>
</li>
<li><strong _msttexthash="6843642" _msthash="562">伪指令</strong>
<ul dir="auto">
<li><font _mstmutation="1" _msttexthash="12437152" _msthash="563"><strong _mstmutation="1" _istranslated="1">基本：</strong></font><code>nop</code></li>
<li><font _mstmutation="1" _msttexthash="23236551" _msthash="564"><strong _mstmutation="1" _istranslated="1">负载</strong>： ，</font><code>la, li</code></li>
<li><font _mstmutation="1" _msttexthash="12055069" _msthash="565"><strong _mstmutation="1" _istranslated="1">OP</strong>的：</font><code>mv, not, neg, negw, sext.b, sext.h, sext.w, zext.b, zext.h, zext.w, seqz, snez, sltz, slgz</code></li>
<li><font _mstmutation="1" _msttexthash="15083406" _msthash="566"><strong _mstmutation="1" _istranslated="1">分公司</strong>：</font><code>beqz, bnez, blez, bgez, bltz, bgtz, bgt, ble, bgtu, bleu</code></li>
<li><font _mstmutation="1" _msttexthash="14721915" _msthash="567"><strong _mstmutation="1" _istranslated="1">跳跃</strong>：</font><code>j, jal, jr, jalr, ret, call, tail</code></li>
</ul>
</li>
<li><strong _msttexthash="4750811" _msthash="568">扩展</strong>
<ul dir="auto">
<li><font _mstmutation="1" _msttexthash="15396693" _msthash="569"><strong _mstmutation="1" _istranslated="1">RV32M/RV64M</strong>：</font><code>mul, mulh, mulhsu, div, divu, rem, remu</code></li>
<li><font _mstmutation="1" _msttexthash="15810249" _msthash="570"><strong _mstmutation="1" _istranslated="1">RV64M</strong> 的：</font><code>mulw, divw, divuw, remw, remuw</code></li>
<li><font _mstmutation="1" _msttexthash="15392325" _msthash="571"><strong _mstmutation="1" _istranslated="1">RV32A/RV64A</strong>：</font><code>lr.w, sc.w, amoswap.w, amoadd.w, amoxor.w, amoand.w, amoor.w, amomin.w, amomax.w, amominu.w, amomaxu.w</code></li>
<li><font _mstmutation="1" _msttexthash="10226515" _msthash="572"><strong _mstmutation="1" _istranslated="1">RV64A</strong>：</font><code>lr.d, sc.d, amoswap.d, amoadd.d, amoxor.d, amoand.d, amoor.d, amomin.d, amomax.d, amominu.d, amomaxu.d</code></li>
<li><font _mstmutation="1" _msttexthash="10249681" _msthash="573"><strong _mstmutation="1" _istranslated="1">Zicsr</strong>：</font><code>csrrw, csrrs, csrrc, csrrwi, csrrsi, csrrci</code></li>
</ul>
</li>
</ul>
<p dir="auto" _msttexthash="144173211" _msthash="574">有关 RISC-V 的详细信息，请参阅 ISA 规范：<a href="https://riscv.org/technical/specifications/" rel="nofollow" _istranslated="1">https://riscv.org/technical/specifications/</a>。</p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto" _msttexthash="45310174" _msthash="575">资源和类似项目的链接</h2><a id="user-content-links-to-resources-and-similar-projects" class="anchor" aria-label="永久链接：资源和类似项目的链接" href="#links-to-resources-and-similar-projects" _mstaria-label="1702428" _msthash="576"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="20247760" _msthash="577">资源和出版物</h3><a id="user-content-resources-and-publications" class="anchor" aria-label="永久链接：资源和出版物" href="#resources-and-publications" _mstaria-label="1084902" _msthash="578"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li>
<p dir="auto" _msttexthash="145483910" _msthash="579">位于布拉格的捷克技术大学的计算机体系结构页面 <a href="https://comparch.edu.cvut.cz/" rel="nofollow" _istranslated="1">https://comparch.edu.cvut.cz/</a></p>
</li>
<li>
<p dir="auto"><font _mstmutation="1" _msttexthash="1571164465" _msthash="580">杜帕克，J.;比萨，P.;斯捷潘诺夫斯基，M.;Koci， K. <a href="https://comparch.edu.cvut.cz/publications/ewC2022-Dupak-Pisa-Stepanovsky-QtRvSim.pdf" rel="nofollow" _mstmutation="1" _istranslated="1">QtRVSim – 用于计算机架构课程的 RISC-V 模拟器</a>：<a href="https://events.weka-fachmedien.de/embedded-world-conference" rel="nofollow" _mstmutation="1" _istranslated="1">2022 年嵌入式世界会议</a>。哈尔：WEKA FACHMEDIEN GmbH，2022 年。第 775-778 页。国际标准书号 978-3-645-50194-1。（<a href="https://comparch.edu.cvut.cz/slides/ewc22-qtrvsim.pdf" rel="nofollow" _mstmutation="1" _istranslated="1">幻灯片</a></font>)</p>
</li>
</ul>
<p dir="auto" _msttexthash="247247286" _msthash="581">如果您在教育或研究相关材料和出版物中使用 QtRvSim，请参考上述文章。</p>
<ul dir="auto">
<li><a href="https://cw.fel.cvut.cz/wiki/courses/b35apo" rel="nofollow" _msttexthash="63878503" _msthash="582">FEE CTU - B35APO - 计算机体系结构</a>
<ul dir="auto">
<li><font _mstmutation="1" _msttexthash="157489254" _msthash="583">本科计算机体系结构类教材 （
捷克语）（<a href="https://cw.fel.cvut.cz/wiki/courses/b35apo/en/start" rel="nofollow" _mstmutation="1" _istranslated="1">英语</a></font>)</li>
</ul>
</li>
<li><a href="https://cw.fel.cvut.cz/wiki/courses/b4m35pap/start" rel="nofollow" _msttexthash="96546879" _msthash="584">FEE CTU - B4M35PAP - 高级计算机体系结构</a>
<ul dir="auto">
<li _msttexthash="162671951" _msthash="585">研究生计算机体系结构课程材料（捷克语/英语）</li>
</ul>
</li>
<li><a href="https://dspace.cvut.cz/bitstream/handle/10467/94446/F3-BP-2021-Dupak-Jakub-thesis.pdf" rel="nofollow" _msttexthash="120866499" _msthash="586">图形化 RISC-V 架构仿真器 - 内存模型和项目管理</a>
<ul dir="auto">
<li _msttexthash="21645598" _msthash="587">Jakub Dupak 的论文</li>
<li _msttexthash="31709639" _msthash="588">文档 2020-2021 QtMips 和 QtRvSim 开发</li>
</ul>
</li>
<li><a href="https://dspace.cvut.cz/bitstream/handle/10467/76764/F3-DP-2018-Koci-Karel-diploma.pdf" rel="nofollow" _msttexthash="73191547" _msthash="589">具有缓存可视化功能的图形 CPU 模拟器</a>
<ul dir="auto">
<li _msttexthash="20425561" _msthash="590">Karel Koci 的论文</li>
<li _msttexthash="21743267" _msthash="591">记录初始 QtMips 开发</li>
</ul>
</li>
</ul>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto" _msttexthash="6718387" _msthash="592">项目</h3><a id="user-content-projects" class="anchor" aria-label="永久链接： Projects" href="#projects" _mstaria-label="372489" _msthash="593"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li>
<p dir="auto" _msttexthash="43697914" _msthash="594"><strong _istranslated="1">QtMips</strong> - 此模拟器<a href="https://github.com/cvut/QtMips/" _istranslated="1">的前身 https://github.com/cvut/QtMips/</a></p>
</li>
<li>
<p dir="auto" _msttexthash="82521283" _msthash="595"><strong _istranslated="1">RARS</strong> - RISC-V 汇编器和运行时
模拟器 <a href="https://github.com/TheThirdOne/rars" _istranslated="1">https://github.com/TheThirdOne/rars</a></p>
</li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto" _msttexthash="5411536" _msthash="596">版权</h2><a id="user-content-copyright" class="anchor" aria-label="永久链接：版权" href="#copyright" _mstaria-label="408707" _msthash="597"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li _msttexthash="33341711" _msthash="598">版权所有 （c） 2017-2019 Karel Koci <a href="mailto:cynerd@email.cz" _istranslated="1">cynerd@email.cz</a></li>
<li _msttexthash="33704086" _msthash="599">版权所有 （c） 2019-2024 Pavel Pisa <a href="mailto:pisa@cmp.felk.cvut.cz" _istranslated="1">pisa@cmp.felk.cvut.cz</a></li>
<li _msttexthash="33603050" _msthash="600">版权所有 （c） 2020-2024 Jakub Dupak <a href="mailto:dev@jakubdupak.com" _istranslated="1">dev@jakubdupak.com</a></li>
<li _msttexthash="33809880" _msthash="601">版权所有 （c） 2020-2021 Max Hollmann <a href="mailto:hollmmax@fel.cvut.cz" _istranslated="1">hollmmax@fel.cvut.cz</a></li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto" _msttexthash="9675445" _msthash="602">许可证</h2><a id="user-content-license" class="anchor" aria-label="永久链接：许可证" href="#license" _mstaria-label="331903" _msthash="603"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font _mstmutation="1" _msttexthash="1139307377" _msthash="604">此项目已获得 许可。许可证的全文位于 <a href="/cvut/qtrvsim/blob/master/LICENSE" _mstmutation="1" _istranslated="1">LICENSE</a> 文件中。这
许可证 适用于除 named 目录及其中的文件之外的所有文件。外部目录中的文件
具有与 Projects 许可证兼容的单独许可证。</font><code>GPL-3.0-or-later</code><code>external</code></p>
<blockquote>
<p dir="auto" _msttexthash="1267578715" _msthash="605">本程序是自由软件：您可以根据自由软件基金会发布的 GNU 通用公共许可证的条款重新分发和/或修改它，无论是许可证的第 3 版，还是（根据您的选择）任何更高版本。</p>
<p dir="auto" _msttexthash="867178702" _msthash="606">分发此程序是希望它有用，但没有任何保证;甚至没有对适销性或特定用途适用性的暗示保证。有关更多详细信息，请参阅 GNU 通用公共许可证。</p>
<p dir="auto" _msttexthash="306656649" _msthash="607">您应该已经收到了 GNU 通用公共许可证的副本以及此程序。如果没有，请参阅 <a href="https://www.gnu.org/licenses/" rel="nofollow" _istranslated="1">https://www.gnu.org/licenses/</a>。</p>
</blockquote>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="/cvut/qtrvsim/blob/master/data/ctu/logo-fee.svg"><img src="/cvut/qtrvsim/raw/master/data/ctu/logo-fee.svg" alt="电气工程学院" style="max-width: 100%;" _mstalt="868114" _msthash="608"></a> <a target="_blank" rel="noopener noreferrer" href="/cvut/qtrvsim/blob/master/data/ctu/logo-fit.svg"><img src="/cvut/qtrvsim/raw/master/data/ctu/logo-fit.svg" alt="资讯科技学院" style="max-width: 100%;" _mstalt="889473" _msthash="609"></a> <a target="_blank" rel="noopener noreferrer" href="/cvut/qtrvsim/blob/master/data/ctu/logo-ctu.svg"><img src="/cvut/qtrvsim/raw/master/data/ctu/logo-ctu.svg" alt="捷克技术大学" style="max-width: 100%;" _mstalt="611845" _msthash="610"></a></p>
</article></div>
