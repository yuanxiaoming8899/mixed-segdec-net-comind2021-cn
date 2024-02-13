<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><h1 tabindex="-1" dir="auto"><a id="user-content-mixed-supervision-for-surface-defect-detection-from-weakly-to-fully-supervised-learning-computers-in-industry-2021" class="anchor" aria-hidden="true" tabindex="-1" href="#mixed-supervision-for-surface-defect-detection-from-weakly-to-fully-supervised-learning-computers-in-industry-2021"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">表面缺陷检测的混合监督：从弱监督学习到完全监督学习 [工业计算机 2021]</font></font></h1>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">PyTorch 的官方实施</font></font><a href="http://prints.vicos.si/publications/385" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">“表面缺陷检测的混合监督：从弱监督学习到完全监督学习”</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">发表在《Computers in Industry 2021》杂志上。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">相同的代码也是2020 年国际模式识别会议上发表的</font></font><a href="http://prints.vicos.si/publications/383" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">“用于缺陷检测的两阶段神经网络的端到端训练”</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">中使用的方法的正式实现。</font></font></p>
<p dir="auto"><a href="http://creativecommons.org/licenses/by-nc-sa/4.0/" rel="nofollow"><img src="https://camo.githubusercontent.com/5254836b4c2097cdf9b882f21a089aa7c06f73b990d36efb5dac7ac41cd764cd/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4c6963656e73652d434325323042592d2d4e432d2d5341253230342e302d6c69676874677265792e737667" alt="CC BY-NC-SA 4.0" data-canonical-src="https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg" style="max-width: 100%;"></a></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">代码和数据集根据</font></font><a href="http://creativecommons.org/licenses/by-nc-sa/4.0/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">获得许可。</font><font style="vertical-align: inherit;">如需商业用途，请联系</font></font><a href="mailto:danijel.skocaj@fri.uni-lj.si"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">danijel.skocaj@fri.uni-lj.si</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<p dir="auto"><a href="http://creativecommons.org/licenses/by-nc-sa/4.0/" rel="nofollow"><img src="https://camo.githubusercontent.com/5de9e83856b6f7835e102b4fbbd467cf53f6c6a2acf9c7f071905e74ba37f1d2/68747470733a2f2f6c6963656e7365627574746f6e732e6e65742f6c2f62792d6e632d73612f342e302f38387833312e706e67" alt="CC BY-NC-SA 4.0" data-canonical-src="https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png" style="max-width: 100%;"></a></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-citation" class="anchor" aria-hidden="true" tabindex="-1" href="#citation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">引文</font></font></h2>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用此代码时，</font><font style="vertical-align: inherit;">请引用我们的</font></font><a href="http://prints.vicos.si/publications/385" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Computers in Industry 2021 论文：</font></font></a><font style="vertical-align: inherit;"></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>@article{Bozic2021COMIND,
  author = {Bo{\v{z}}i{\v{c}}, Jakob and Tabernik, Domen and 
  Sko{\v{c}}aj, Danijel},
  journal = {Computers in Industry},
  title = {{Mixed supervision for surface-defect detection: from weakly to fully supervised learning}},
  year = {2021}
}
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="@article{Bozic2021COMIND,
  author = {Bo{\v{z}}i{\v{c}}, Jakob and Tabernik, Domen and 
  Sko{\v{c}}aj, Danijel},
  journal = {Computers in Industry},
  title = {{Mixed supervision for surface-defect detection: from weakly to fully supervised learning}},
  year = {2021}
}" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<h2 tabindex="-1" dir="auto"><a id="user-content-how-to-run" class="anchor" aria-hidden="true" tabindex="-1" href="#how-to-run"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如何运行：</font></font></h2>
<h3 tabindex="-1" dir="auto"><a id="user-content-requirements" class="anchor" aria-hidden="true" tabindex="-1" href="#requirements"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要求</font></font></h3>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">代码已经过测试，可用于：</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Python 3.8</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">火炬 1.6、1.8</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">CUDA 10.0、10.1</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用requirements.txt中列出的附加包</font></font></li>
</ul>
<h3 tabindex="-1" dir="auto"><a id="user-content-datasets" class="anchor" aria-hidden="true" tabindex="-1" href="#datasets"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">数据集</font></font></h3>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您需要自己下载数据集。</font><font style="vertical-align: inherit;">对于 DAGM 和 Severstal Steel 缺陷数据集，您还需要一个 Kaggle 帐户。</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">DAGM 可</font></font><a href="https://www.kaggle.com/mhskjelvareid/dagm-2007-competition-dataset-optical-inspection" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在此处获取。</font></font></a></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">KolektorSDD 可</font></font><a href="https://www.vicos.si/Downloads/KolektorSDD" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在此处获取。</font></font></a></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">KolektorSDD2 可</font></font><a href="https://www.vicos.si/Downloads/KolektorSDD2" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在此处获取。</font></font></a></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">谢韦尔钢铁缺陷数据集可</font></font><a href="https://www.kaggle.com/c/severstal-steel-defect-detection/data" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在此处获取。</font></font></a></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">有关数据结构的详细信息，请参阅文件夹</font></font><code>README.md</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">中的内容</font></font><code>datasets</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">所有数据集的交叉验证拆分、训练/测试拆分和弱/完全标记拆分都位于</font></font><code>splits</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">此存储库的目录中，以及有关如何使用它们的说明。</font></font></p>
<h5 tabindex="-1" dir="auto"><a id="user-content-using-on-other-data" class="anchor" aria-hidden="true" tabindex="-1" href="#using-on-other-data"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">用于其他数据</font></font></h5>
<p dir="auto"><font style="vertical-align: inherit;"></font><code>README.md</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">有关</font></font><code>datasets</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如何在其他数据集上使用该方法的说明，</font><font style="vertical-align: inherit;">请参阅。</font></font></p>
<h3 tabindex="-1" dir="auto"><a id="user-content-demo---fully-supervised-learning" class="anchor" aria-hidden="true" tabindex="-1" href="#demo---fully-supervised-learning"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">演示 - 完全监督学习</font></font></h3>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要对所有四个数据集运行完全监督的学习和评估，请运行：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>./DEMO.sh
<span class="pl-c"><span class="pl-c">#</span> or by specifying multiple GPU ids </span>
./DEMO.sh 0 1 2</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="./DEMO.sh
# or by specifying multiple GPU ids 
./DEMO.sh 0 1 2" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">结果将写入</font></font><code>./results</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文件夹。</font></font></p>
<h3 tabindex="-1" dir="auto"><a id="user-content-replicating-paper-results" class="anchor" aria-hidden="true" tabindex="-1" href="#replicating-paper-results"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">复制论文结果</font></font></h3>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要复制论文中发布的结果，请执行以下操作：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>./EXPERIMENTS_COMIND.sh
<span class="pl-c"><span class="pl-c">#</span> or by specifying multiple GPU ids </span>
./EXPERIMENTS_COMIND.sh 0 1 2</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="./EXPERIMENTS_COMIND.sh
# or by specifying multiple GPU ids 
./EXPERIMENTS_COMIND.sh 0 1 2" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">复制</font></font><a href="http://prints.vicos.si/publications/383" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">ICPR 2020 论文</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">的结果：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>@misc{Bozic2020ICPR,
    title={End-to-end training of a two-stage neural network for defect detection},
    author={Jakob Božič and Domen Tabernik and Danijel Skočaj},
    year={2020},
    eprint={2007.07676},
    archivePrefix={arXiv},
    primaryClass={cs.CV}
}
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="@misc{Bozic2020ICPR,
    title={End-to-end training of a two-stage neural network for defect detection},
    author={Jakob Božič and Domen Tabernik and Danijel Skočaj},
    year={2020},
    eprint={2007.07676},
    archivePrefix={arXiv},
    primaryClass={cs.CV}
}" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">跑步：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>./EXPERIMENTS_ICPR.sh
<span class="pl-c"><span class="pl-c">#</span> or by specifying multiple GPU ids </span>
./EXPERIMENTS_ICPR.sh 0 1 2
</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="./EXPERIMENTS_ICPR.sh
# or by specifying multiple GPU ids 
./EXPERIMENTS_ICPR.sh 0 1 2
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">结果将写入</font></font><code>./results-comind</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和</font></font><code>./results-icpr</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文件夹。</font></font></p>
<h3 tabindex="-1" dir="auto"><a id="user-content-usage-of-trainingevaluation-code" class="anchor" aria-hidden="true" tabindex="-1" href="#usage-of-trainingevaluation-code"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">培训/评估代码的使用</font></font></h3>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">以下 python 文件用于训练/评估模型：</font></font></p>
<ul dir="auto">
<li><code>train_net.py</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">培训与评估主入口</font></font></li>
<li><code>models.py</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">网络模型文件</font></font></li>
<li><code>data/dataset_catalog.py</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">包含当前支持的数据集</font></font></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">为了训练和评估网络，您还可以使用</font></font><code>EXPERIMENTS_ROOT.sh</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，其中包含多个函数，可以使您更轻松地进行训练和评估。</font><font style="vertical-align: inherit;">有关更多详细信息，请参阅该文件</font></font><code>EXPERIMENTS_ROOT.sh</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<h4 tabindex="-1" dir="auto"><a id="user-content-running-code" class="anchor" aria-hidden="true" tabindex="-1" href="#running-code"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">运行代码</font></font></h4>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">训练和评估网络的最简单方法是使用，您可以在</font><font style="vertical-align: inherit;">和 中</font></font><code>EXPERIMENTS_ROOT.sh</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">查看使用示例</font></font><code>EXPERIMENTS_ICPR.sh</code><font style="vertical-align: inherit;"></font><code>EXPERIMENTS_COMIND.sh</code></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您希望以其他方式执行此操作，可以通过运行</font></font><code>train_net.py</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">并将参数作为关键字参数传递来实现。</font><font style="vertical-align: inherit;">下面是如何为单倍数据集训练模型的示例</font></font><code>KSDD</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>python -u train_net.py  \
    --GPU=0 \
    --DATASET=KSDD \
    --RUN_NAME=RUN_NAME \
    --DATASET_PATH=/path/to/dataset \
    --RESULTS_PATH=/path/to/save/results \
    --SAVE_IMAGES=True \
    --DILATE=7 \
    --EPOCHS=50 \
    --LEARNING_RATE=1.0 \
    --DELTA_CLS_LOSS=0.01 \
    --BATCH_SIZE=1 \
    --WEIGHTED_SEG_LOSS=True \
    --WEIGHTED_SEG_LOSS_P=2 \
    --WEIGHTED_SEG_LOSS_MAX=1 \
    --DYN_BALANCED_LOSS=True \
    --GRADIENT_ADJUSTMENT=True \
    --FREQUENCY_SAMPLING=True \
    --TRAIN_NUM=33 \
    --NUM_SEGMENTED=33 \
    --FOLD=0
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python -u train_net.py  \
    --GPU=0 \
    --DATASET=KSDD \
    --RUN_NAME=RUN_NAME \
    --DATASET_PATH=/path/to/dataset \
    --RESULTS_PATH=/path/to/save/results \
    --SAVE_IMAGES=True \
    --DILATE=7 \
    --EPOCHS=50 \
    --LEARNING_RATE=1.0 \
    --DELTA_CLS_LOSS=0.01 \
    --BATCH_SIZE=1 \
    --WEIGHTED_SEG_LOSS=True \
    --WEIGHTED_SEG_LOSS_P=2 \
    --WEIGHTED_SEG_LOSS_MAX=1 \
    --DYN_BALANCED_LOSS=True \
    --GRADIENT_ADJUSTMENT=True \
    --FREQUENCY_SAMPLING=True \
    --TRAIN_NUM=33 \
    --NUM_SEGMENTED=33 \
    --FOLD=0" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">某些数据集不需要您指定</font></font><code>--TRAIN_NUM</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">或</font></font><code>--FOLD</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- 训练后，还会评估每个模型。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对于 KSDD，您需要结合所有三个方面的评估结果，您可以使用以下方法来完成此操作</font></font><code>join_folds_results.py</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>python -u join_folds_results.py \
    --RUN_NAME=SAMPLE_RUN \
    --RESULTS_PATH=/path/to/save/results \
    --DATASET=KSDD 
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python -u join_folds_results.py \
    --RUN_NAME=SAMPLE_RUN \
    --RESULTS_PATH=/path/to/save/results \
    --DATASET=KSDD " tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您可以使用它</font></font><code>read_results.py</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">来生成所选数据集的所有运行的结果表。</font><font style="vertical-align: inherit;">注意：模型对训练过程中的随机初始化和数据洗牌很敏感，除非设置</font></font><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
，否则将导致不同运行的不同性能。</font></font><code>--REPRODUCIBLE_RUN</code><font style="vertical-align: inherit;"></font></p>
</article></div>
