---
layout: page
title: Home
permalink: /home/
---


<article class="post post-40 page type-page status-publish hentry" id="post-40">
    <div class="entry clearfix">
      <div id="main">
<div id="container" class="two-column">
<div id="content" role="main">
<h2 class="entry-title">OSHMPI : OpenSHMEM Implementation on MPI</h2>
<div class="entry-content">
<p>OpenSHMEM is an increasingly popular standard of the SHMEM programming model. There are many different OpenSHMEM implementations such as Sandia OpenSHMEM, OSHMEM in Open MPI, Cray SHMEM etc. Many of these implementations utilize only one or a few network providers and platforms.</p>
<p>On the other hand, MPI has been the de facto standard for parallel programming for more than 2 decades. Popular MPI implementations provide good performance on supports a wide range of platforms. To leverage MPI’s performance and portability, we attempt to build an OpenSHMEM implementation on top of MPI, called <em><strong>OSHMPI</strong></em>.</p>
<div style="text-align: certer"><img class="alignnone wp-image-222" src="http://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.12.57-PM-300x91.png" alt="" width="597" height="181" srcset="https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.12.57-PM-300x91.png 300w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.12.57-PM-768x233.png 768w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.12.57-PM-1024x310.png 1024w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.12.57-PM-220x67.png 220w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.12.57-PM.png 1308w" sizes="(max-width: 597px) 100vw, 597px"></div>

<p style="margin-bottom: 1px"><strong><span style="color: #4d7508;font-size: 13pt">Key Features</span></strong></p>
<ul>
<li style="list-style-type: none">
<ul>
<li>Full support of OpenSHMEM specification 1.4.</li>
<li>Function inline for all OSHMPI internal routines.</li>
<li>Caching internal MPI communicators for collective operations with PE active set.</li>
<li>OpenSHMEM multithreading safety support.</li>
<li>Active message support of OpenSHMEM atomic operations. MPI accumulates cannot be directly used because MPI does not guarantee atomicity between different reduce operations.</li>
<li>Optional asynchronous progress thread support for active message based atomic.</li>
</ul>
</li>
</ul>

<p style="margin-bottom: 1px"><strong><span style="color: #4d7508;font-size: 13pt">Portability Showcase</span></strong></p>
<ul>
<li style="list-style-type: none">
<ul>
<li>Figure below compares OSHMPI against various OpenSHMEM implementations on their respective target platforms.</li>
</ul>
</li>
</ul>
<p><img class="alignnone wp-image-228" src="http://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.17.49-PM-300x184.png" alt="" width="540" height="331" srcset="https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.17.49-PM-300x184.png 300w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.17.49-PM-768x472.png 768w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.17.49-PM-1024x629.png 1024w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.17.49-PM-220x135.png 220w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.17.49-PM.png 1156w" sizes="(max-width: 540px) 100vw, 540px"></p>

<p style="margin-bottom: 1px"><strong><span style="color: #4d7508;font-size: 13pt">Performance Showcase</span></strong></p>
<ul>
<li style="list-style-type: none">
<ul>
  <li>OSHMPI achieves comparable latency and message rate to Sandia OpenSHMEM (SOS) using OFI/psm2 on an Intel Omni-path cluster.</li>
  <li>OSHMPI is also close to the pure communication performance which is shown by using only the native OFI write/read operations.</li>
  
</ul>
</li>
</ul>
  <li style="list-style-type: none"><img class="alignnone wp-image-224" src="http://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.14.45-PM-300x187.png" alt="" width="528" height="329" srcset="https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.14.45-PM-300x187.png 300w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.14.45-PM-768x478.png 768w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.14.45-PM-1024x638.png 1024w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.14.45-PM-220x137.png 220w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.14.45-PM.png 1130w" sizes="(max-width: 528px) 100vw, 528px"><br>
<img class="alignnone wp-image-226" src="http://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.15.38-PM-300x173.png" alt="" width="517" height="298" srcset="https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.15.38-PM-300x173.png 300w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.15.38-PM-768x442.png 768w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.15.38-PM-1024x590.png 1024w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.15.38-PM-220x127.png 220w, https://www.mcs.anl.gov/project/oshmpi/files/2018/11/Screen-Shot-2018-11-12-at-1.15.38-PM.png 1212w" sizes="(max-width: 517px) 100vw, 517px"></li>
</div>
</div>
</div>
</div>
      
            
          </div>
    	<div id="comments">
	
	
	
	
</div><!-- #comments -->  </article>