While employed at [Square Enix](https://en.wikipedia.org/wiki/Square_Enix), Japan, I partecipated in the development of a next generation 3D engine capable of optimizing production rendering scenes and reproducing them in real-time with Direct3D and many-core hardware.

The engine supported very high resolution geometry and multi-gigabyte textures as well as per-vertex animation.
I wrote rendering and compression technology capable of reducing computing and storage for the target hardware.
Rendering was performed with Direct3D 10. Compression used lossy approaches based on DCT, Wavelets and Zero-tree encoding.

![]({{ site.baseurl }}/images/zzz_demo_tv_nhk_program.jpg)
![]({{ site.baseurl }}/images/zzzdemo_rtpic_03.png){:width="50%"} ![]({{ site.baseurl }}/images/zzzdemo_rtpic_01.png){:width="50%"}

#### My work on the project

I was the lead engineer on the runtime portion of the project. My main tasks were:

- Research & Develop new technology to handle massive production-rendering assets in real-time
- Writing the runtime rendering engine in Direct3D
- Writing custom GPGPU-friendly CODECs for texture and 3D geometry compression and streaming
- Working with hardware manufacturers to optimize graphics drivers

#### What I learned

- Multiprocessor and advanced SIMD architectures
- Maximizing performance around graphics drivers
- Managing and optimizing large 3D assets for production rendering
- Geometry compression techniques
- Team and project management
