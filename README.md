为了更好的阅读请在**[gitbook](https://xhunmon.github.io/VABlog/)** 阅读

# 一、前言
随着时代的发展，各种短视频、直播、语音客服等等走进了各行各业！而未来5g/6g技术普及的时候，音视频要成为每个项目的标配！而本人在学习过程中整理了学习笔记和各方面的学习资料。

# 二、学习技能

| 技能        | 重要度 | 作用                                                         | 学习建议                                 |
| ----------- | ------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| c/c++       | ★★★★☆  | 音视频开源库基本都是用c/c++写的，如：FFmpeg库用C语言写的，Webrtc底层是用c\+\+写的。 | 1. 看视频（最后）；2. 看书：c\+\+ primer 第5版；3. 看FFmpeg源码；4. 最重要自己动手敲。 |
| cmake       | ★★★☆☆  | 跨平台引导编译的重要语言。在CMakeList.txt文件体现。          | 1. 看动脑CMake中视频（最后）；2. [CMake 入门实战](https://www.hahack.com/codes/cmake/) |
| shell       | ★★☆☆☆  | 很多开源库都是通过shell脚本进行编译的。如ffmpeg和x264中configure。 |  [Shell脚本](./FFmpeg/02_shell.md) |
| Android NDK | ★★☆☆☆  | 在android平台上使用，需要掌握NDK的一些知识。如：交叉编译，JNI的接入。 | 看动脑NDK中JNI和交叉编译视频（最后）；                            |
| IOS         | ★★☆☆☆  | （略）                                                       | （略）                                                       |

# 三、学习音视频理论知识
- [书：音视频开发进阶指南：基于Android与iOS平台的实践(京东)](https://item.jd.com/12292642.html) ：**第1章　音视频基础概念**；电子书往最后翻。
- [书：Android 音视频开发_何俊林(京东)](https://item.jd.com/12467530.html) ：**第1章　音视频基础知识**；电子书往最后翻。
- [书：新一代视频压缩编码标准-H.264/AVC(第二版)(京东)](https://item.jd.com/10022441804147.html) : 讲述H.264等编解码原理实现，其中几个算法 [这篇文章](https://zhuanlan.zhihu.com/p/40356456)讲的很深刻。
- 也可以在[这里1](https://www.dalipan.com/) 或者[这里2](https://ebook2.lorefree.com/) 搜索。
- [这系列文章通俗易懂讲述编解码的一些知识](http://www.52im.net/thread-228-1-1.html)。


# 四、学习音视频基本原理
## 1）视音频数据处理入门
[[总结]视音频编解码技术零基础学习方法](https://blog.csdn.net/leixiaohua1020/article/details/18893769) 系列文章，介绍了视音频编解码技术大体上原理和流程，通俗易懂。包括以下文章：
- [视音频数据处理入门：RGB、YUV像素数据处理](https://blog.csdn.net/leixiaohua1020/article/details/50534150) ：视频就是由它们组成的。
- [视音频数据处理入门：PCM音频采样数据处理](https://blog.csdn.net/leixiaohua1020/article/details/50534316) ：音频就是由它们组成的。
- [视音频数据处理入门：H.264视频码流解析](https://blog.csdn.net/leixiaohua1020/article/details/50534369) ：视频编码技术的一种（现代音视频开发必须掌握）。
- [视音频数据处理入门：AAC音频码流解析](https://blog.csdn.net/leixiaohua1020/article/details/50535042) ：音频编码技术的一种（现代音视频开发必须掌握）。
- [视音频数据处理入门：FLV封装格式解析](https://blog.csdn.net/leixiaohua1020/article/details/50535082) ：音视频封装格式的一种。
- [视音频数据处理入门：UDP-RTP协议解析](https://blog.csdn.net/leixiaohua1020/article/details/50535230) ：音视频协议的一种。

## 2）完整的RTMP推送小项目
- [直播推流全过程：总纲](直播推流全过程/README.md)
- [直播推流全过程：视频数据源之YUV](直播推流全过程/1-yuv.md)
- [直播推流全过程：音频数据源之PCM](直播推流全过程/2-pcm.md)
- [直播推流全过程：视频编码之H.264](直播推流全过程/3-h264.md)
- [直播推流全过程：音频编码之AAC](直播推流全过程/4-aac.md)
- [直播推流全过程：直播推流编码之RTMP](直播推流全过程/5-rtmp.md)
- [其他：H.264符号描述](直播推流全过程/h264-descriptor.md)
- [其他：直播优化基础](直播推流全过程/6-optimize.md)


# 五、学习FFmpeg
音视频开发是绕不开FFmpeg的，因为它是一个"集大成者"，里面已经包含或可集成现代几乎所有的音视频技术（库）。

## 1）学习途径
- [阅读官方文档](http://ffmpeg.org/ffmpeg.html)
- 学习官方例子（源码中`doc/examples/xxx`）
- [[总结]FFMPEG视音频编解码零基础学习方法](https://blog.csdn.net/leixiaohua1020/article/details/15811977)
- 书籍（电子书往最后翻）
> - [1.FFmpeg从入门到精通(京东)](https://item.jd.com/12349436.html)
> - [2.FFMPEG_FFPLAY源码剖析(CSDN)](https://download.csdn.net/detail/leixiaohua1020/6377803)
> - [3.音视频开发进阶指南：基于Android与iOS平台的实践(京东)](https://item.jd.com/12292642.html)
> - [4.Android 音视频开发_何俊林(京东)](https://item.jd.com/12467530.html) 

## 2）学习路线
[这里不推荐直接学习雷神的 [总结]FFMPEG视音频编解码零基础学习方法，建议是通过在学习FFmpeg官方例子中进行学习，避免先入为主使用了过时的API。](https://blog.csdn.net/leixiaohua1020/article/details/15811977)

### a) 源码编译
[编译ffmpeg4.2.2](./FFmpeg/03_build_ffmpeg.md)通过这篇文章我们基本可以编译出我们想要的FFmpeg库

### b) 源码阅读
- 源码导入：[FFmpeg导入到Clion（MacOS）](./FFmpeg/04_import_ffmpeg.md) 、 [使用Clion阅读FFmpeg源码（支持跳转）](./FFmpeg/05_source.md) 
- 阅读参考：[FFMPEG_FFPLAY源码剖析(CSDN)](https://download.csdn.net/detail/leixiaohua1020/6377803) 、[雷神的FFmpeg源代码系列](https://blog.csdn.net/leixiaohua1020/article/details/44220151) 

### c) 学习官方例子
- [FFmpeg重要结构体（转载）](./FFmpeg/06_struct.md) ，因为在学习FFmpeg中，必须得知道结构体中重要参数的含义，否则举步维艰。
- [FFmpeg Demuxing（解封装）](./FFmpeg/08_demuxing.md) 对应 `doc/examples/demuxing_decoding.c` 中的解封装部分。 
- [FFmpeg Muxing（封装）](./FFmpeg/09_muxing.md) 对应 `doc/examples/muxing.c` 。
- [FFmpeg Remuxing（重新封装）](./FFmpeg/10_remuxing.md) 对应 `doc/examples/remuxing.c` 。
- [FFmpeg Decode（解码）](./FFmpeg/11_decode.md) 对应 `doc/examples/decode_audio.c` 和 `doc/examples/decode_video.c` 。
- [FFmpeg Encode（编码）](./FFmpeg/12_encode.md) 对应 `doc/examples/encode_audio.c` 和 `doc/examples/encode_video.c` 。
- [FFmpeg 简单实现转码](./FFmpeg/13_transfer.md) 汇总解封装、解码、编码、封装放到一起方便理解 。
- [FFmpeg Filter和SDL（Video）](./FFmpeg/14_filter_v.md) 对应 `doc/examples/filtering_video.c` 。
- [FFmpeg Filter和SDL（Audio）](./FFmpeg/15_filter_a.md) 对应 `doc/examples/filtering_video.c` 。
- [FFmpeg Transcode(转码)](./FFmpeg/16_transcode.md) 对应 `doc/examples/transcoding.c` 。
- [FFmpeg Swscale（图像转换）](./FFmpeg/19_swscale.md) 对应 `doc/examples/scaling_video.c` 。

### d) 音视频同步
- [FFmpeg 音视频同步处理](./FFmpeg/17_sync.md)

## 3）FFmpeg相关
- [FFmpeg 命令使用指南：分析ffmpeg、ffprobe、ffplay工具使用文档，关联官方文档，以及滤镜、协议、视频合并、各种播放参数等相关介绍](./FFmpeg/18_command.md)

# 六、OpenGL
OpenGL使用GPU渲染视频，释放宝贵的CPU资源，学习它是必不可少的。但是，正如[雷神所说](https://blog.csdn.net/leixiaohua1020/article/details/40246783) ：作为一个搞视频技术的人研究OpenGL，需要耗费大量时间和精力，这样学习不是很经济。所以推荐只学习有关视频渲染相关知识。
- [OpenGL介绍，和相关程序库](https://zh.wikipedia.org/wiki/OpenGL)
- [纹理有关的基础知识](https://blog.csdn.net/leixiaohua1020/article/details/40301179) 、[OpenGL播放RGB/YUV](https://blog.csdn.net/leixiaohua1020/article/details/40333583) 、[OpenGL播放YUV420P（通过Texture，使用Shader）](https://blog.csdn.net/leixiaohua1020/article/details/40379845)
- [Android OpenGL ES官方文档](https://developer.android.google.cn/guide/topics/graphics/opengl?hl=zh_cn)
- [LearnOpenGL-CN](https://github.com/LearnOpenGL-CN/LearnOpenGL-CN)
- [OpenGL电子书下载](https://github.com/Canber/OpenGL-ES-for-android)
- [OpenGL基础知识](./OpenGL/01_opengl.md)
- [AFPlayer：OpenGL ES播放RGB](./AFPlayer/02_opengl_es.md)

# 七、其他

- [AFPlayer项目](./AFPlayer/README.md) Android实现FFmpeg、OpenSL ES、OpenGL SE、MediaCodec等，实现简单的播放器，主要体现出相关知识点的使用。

- [手撕FLV协议](./FFmpeg/07_flv.md) 。

#八、最后
若有帮助就Star一下呗，您的鼓励是我开源的动力！

# [音视频学习资料](https://pan.baidu.com/s/1Y5PFgbVu3W0ELBgQnrHNYA)
**创作皆不易，有条件的朋友请支持原版，谢谢！**
> - 密码:lqi9
> - FFmpeg命令大全.docx
> - ffmpeg命令大全.pdf
> - 《FFmpeg_Basics(260页)》.pdf
> - webrtc介绍.pdf
> - 价值几千块的音视频视频
> - 动脑视频
> - 网易视频
> - C++侯捷视频
> - Advanced C and C++ Compiling.pdf
> - Android 音视频开发_何俊林.pdf
> - C Primer中文版 第五版 .pdf
> - C++ Primer Plus（第6版）中文版.azw3
> - C++ Primer(第5版)中文版.pdf
> - FFMPEG_FFPLAY源码剖析.7z
> - H.264-AVC-ISO_IEC_14496-10.pdf
> - H.264-AVC-ISO_IEC_14496-15.pdf
> - H.264_MPEG-4-Part-10-White-Paper.pdf
> - H.264官方中文版.pdf
> - ISO_IEC-14496-3-2009.pdf
> - ISO_IEC_14496-14_2003-11-15.pdf
> - SDL2-API手册.doc
> - aac-iso-13818-7.pdf
> - STL源码剖析简体中文完整版(清晰扫描带目录).pdf
> - amf0_spec_121207.pdf
> - amf3_spec_121207.pdf
> - hls-m3u8-draft-pantos-http-live-streaming-12.txt
> - hls-mpeg-ts-VB_WhitePaper_TransportStreamVSProgramStream_rd2.pdf
> - hls-mpeg-ts-iso13818-1.pdf
> - rtmp.part1.Chunk-Stream.pdf
> - rtmp.part2.Message-Formats.pdf
> - rtmp.part3.Commands-Messages.pdf
> - rtmp规范翻译1.0.docx
> - rtmp_specification_1.0.pdf
> - video_file_format_spec_v10_1.pdf
> - 《FFmpeg从入门到精通》.pdf
> - 数字信号处理教程（第四版）.pdf
> - 新一代视频压缩编码标准-H.264_AVC(第二版).pdf
> - 音视频开发进阶指南：基于Android与iOS平台的实践.pdf

---------------------------------------------
本文资料一切皆从网络而来，如有侵权请联系我（邮箱：xhunmon@126.com）进行删除。
