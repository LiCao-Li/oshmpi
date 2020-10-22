---
layout: page
permalink: /quick_start/
---

<article class="post post-72 page type-page status-publish hentry" id="post-72">
        <header class="post-header">
      <h2 class="post-title">
        quick-start      </h2>
       
    </header>
   
    <div class="entry clearfix">
      <div style="padding-top: 5px;border-top: 3px solid #4d7508">
<ol>
<li><strong>Installation</strong>
<pre style="border: 1px solid gray;padding: 5 5 5 5px">./configure --prefix=/your/oshmpi/inst/path CC=/path/to/mpicc
make
make install
</pre>
</li>
<li><strong>Compile an OpenSHMEM Program</strong>
<pre style="border: 1px solid gray;padding: 5 5 5 5px">/your/oshmpi/inst/path/bin/oshcc -o test test.c
</pre>
<p style="margin-bottom: 1px">Or</p>
<pre style="border: 1px solid gray;padding: 5 5 5 5px">/your/oshmpi/inst/path/bin/oshc++ -o test test.cpp
</pre>
</li>
<li><strong>Execution</strong>
<p style="margin-bottom: 1px">Running OpenSHMEM program with 2 PEs using mpiexec.</p>
<pre style="border: 1px solid gray;padding: 5 5 5 5px">/path/to/mpiexec -np 2 ./test
</pre>
<p style="margin-bottom: 1px">For more information about the mpiexec command, please check the MPI library’s documentation.</p>
</li>
</ol>
</div>
      
            
          </div>
    	<div id="comments">
	
	
	
	
</div><!-- #comments -->  </article>