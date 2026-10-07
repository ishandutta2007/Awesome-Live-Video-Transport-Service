# Awesome-Live-Video-Transport-Service

## Top Live Video Transport Service Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Contribution Protocols, Low-Latency Transport & Self-Hosted Media Gateways*  

**Last updated: October 2026**



This repository tracks notable **commercial live video transport platforms** and **open-source projects** that reliably move broadcast-quality video over IP networks — from contribution feeds and remote production workflows to cloud-based routing and distribution without packet loss or latency degradation.



**Examples** include AWS Elemental MediaConnect, Zixi Cloud, Haivision SRT Gateway, LiveU Cloud, TVU Networks, LTN Global, VideoFlow, Red Bee Media, Grass Valley AMPP, and Synamedia Video Network (the category leaders).



**Open-source emphasis**: Live video transport is anchored by **SRT** and **RIST** as the two major open protocols for reliable contribution over lossy networks, with **HydraSRT** providing an open-source alternative to Haivision's commercial SRT Gateway . **IRLServer** delivers a full suite of SRT/RIST tooling including OBS plugins and bonding senders . **ts-transformer** brings typed MPEG-TS and KLV metadata transport over SRT, RIST, and RTP . **MediaMTX** provides zero-dependency multi-protocol media routing . **FFmpeg** and **GStreamer** underpin most transport pipelines . This section is heavily expanded.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[AWS Elemental MediaConnect](https://aws.amazon.com/mediaconnect/)**  

  **AWS's managed live video transport service** — reliable, secure, and flexible transport for broadcast and streaming workflows . **Supports RIST, SRT, Zixi, RTP, and CDI protocols** for contribution and distribution . **Pay-as-you-go pricing** with no upfront commitment . **Best for AWS-native live video contribution** .



- **[Zixi Cloud](https://zixi.com/)**  

  **The pioneer of reliable internet transport** — content-aware FEC and ARQ with dynamic de-jitter buffers . **SMPTE 2022-7 hitless redundancy and bonding** with primary/standby paths . **Interoperability with 100+ partners and OEMs** across 10,000+ live video channels in 100+ countries  . **Best for enterprise broadcast contribution at scale** .



- **[Haivision SRT Gateway](https://www.haivision.com/)**  

  **Commercial SRT routing and gateway** — the reference implementation for SRT-based contribution . **SRT protocol originally developed and open-sourced by Haivision**  . **Best for SRT-native workflows** .



- **[LiveU Cloud](https://www.liveu.tv/)**  

  **Cloud-based live video contribution** — cellular bonding and remote production . **Best for field contribution and remote production** .



- **[TVU Networks](https://www.tvunetworks.com/)**  

  **Live video transmission and remote production** — cellular bonding and cloud workflows . **Best for newsgathering and live events** .



- **[LTN Global](https://ltnglobal.com/)**  

  **Managed IP video transport** — reliable contribution and distribution for broadcasters . **Best for global broadcast transport** .



- **[VideoFlow](https://www.videoflow.tv/)**  

  **Reliable video transport with adaptive rate control** — waived its ARQ patent for RIST industry adoption  . **Best for broadcast-grade reliability** .



- **[Red Bee Media](https://www.redbeemedia.com/)**  

  **Broadcast managed services** — contribution, distribution, and media management . **Best for managed broadcast services** .



- **[Grass Valley AMPP](https://www.grassvalley.com/)**  

  **Cloud-native media production platform** — live contribution and remote production . **Best for cloud-based production workflows** .



- **[Synamedia Video Network](https://www.synamedia.com/)**  

  **Video network solutions** — contribution, distribution, and edge processing . **Best for pay-TV and broadcast operators** .



## Open-Source GitHub Projects



### Reliable Transport Gateways



- **[HydraSRT](https://github.com/streamband/hydra-srt)**  

  **An open-source alternative to Haivision SRT Gateway**, Apache-2.0 licensed . **Supports SRT, UDP, RTMP, RTP, NDI, and YouTube as inputs**; **SRT, UDP, RTMP, and NDI as outputs** . **Built with Elixir/OTP for fault isolation, Rust + GStreamer for media processing, and React for UI** . **Source failover with primary + backup sources, automatic failover, and manual switching** . **SRT authentication with passphrase and stream ID** . **Prometheus metrics and VictoriaMetrics/VictoriaLogs for observability** . **Docker deployment with web UI** . **Beta status but production-oriented architecture**  . **Best for open-source SRT gateway deployment** .



### SRT/RIST Tooling



- **[IRLServer](https://github.com/irlserver)**  

  **Suite of open-source tools for IRL streaming with SRT and RIST**, various licenses (AGPL-3.0, MIT, MPL-2.0) . **Key repositories**: **obs-irl-source** — OBS plugin for receiving live IRL streams over SRT, RTMP, RIST, or any FFmpeg-supported protocol (Rust) . **srtla_send** — SRTLA bonding sender in Rust aggregating bandwidth across multiple network paths . **srtla** — SRT transport proxy with link aggregation for connection bonding (C++) . **irl-srt-server** — SRT Live Server for low-latency streaming with SRTLA/Belabox support (C++) . **librist** — customized VideoLAN library for RIST protocol (C)  . **Best for IRL and field contribution with SRT/RIST** .



- **[ts-transformer](https://github.com/aklofas/ts-transformer)**  

  **Streams live H.264/H.265 video plus typed KLV metadata over unreliable networks in ~30 lines of code**, open-source . **Transport support: SRT, RTP, TCP, UDP, and RIST** . **MPEG-TS with MISB ST 0601 (UAS Datalink), ST 0102 (Security), ST 0605 (Precision Time Stamp), and ST 0903 (VMTI) KLV metadata** . **Rust core with C, Python, and JVM bindings** . **Reconnect, encryption, and typed metadata decoding handled** . **Transmux for editing metadata while copying video/audio byte-for-byte**  . **Best for sensor and ISR video transport** .



### Multi-Protocol Media Routers



- **[MediaMTX](https://github.com/bluenviron/mediamtx)**  

  **Ready-to-use zero-dependency live media server and media proxy**, MIT licensed . **Supports Media-over-QUIC, SRT, WebRTC, RTSP, RTMP, LL-HLS, MPEG-TS, and RTP** . **Automatic protocol conversion** — streams are converted from one protocol to another . **Single executable, no dependencies** . **Raspberry Pi camera support** . **Best for edge and simple deployments**  .



- **[SRS (Simple Realtime Server)](https://github.com/ossrs/srs)**  

  **The leading open-source live streaming server**, MIT/MulanPSL-2.0 licensed with **29,206+ GitHub stars** . **Supports RTMP, WebRTC, HLS, HTTP-FLV, SRT, MPEG-DASH** . **RTMP latency 0.8–3s**; **min-latency mode ~0.1s for video-only** . **Scalable to millions of viewers** . **The de facto open-source Wowza alternative**  . **Best for production live streaming and relay** .



- **[Janus WebRTC Server](https://github.com/meetecho/janus-gateway)**  

  **General-purpose WebRTC gateway with protocol translation**, GPL-3.0 licensed with **9,159+ GitHub stars** . **Plugin architecture for VideoRoom, SIP, streaming** . **Converts WebRTC streams into legacy formats such as SIP** . **Best for WebRTC-to-legacy protocol bridging**  .



### Protocol Implementations



- **[SRT (Secure Reliable Transport)](https://github.com/Haivision/srt)**  

  **Open-source video transport protocol and technology stack**, MPL-2.0 licensed . **Optimizes streaming performance across unpredictable networks** with ARQ, encryption (AES 128/256), and firewall traversal . **The SRT Open Source project driven by Haivision and the SRT Alliance with 100+ industry members**  . **Best for low-latency contribution over lossy networks** .



- **[libRIST](https://code.videolan.org/rist/librist)**  

  **Open-source implementation of the RIST protocol**, BSD-2-Clause licensed . **RIST Main Profile with SMPTE 2022-1 FEC** for low-latency error recovery . **Firewall traversal (sender only)** . **Supports multicast and bonding** . **Enhanced Profile under development** adds smart bandwidth optimization and hybrid internet/satellite operation  . **Best for vendor-neutral reliable transport** .



- **[Project-Lightspeed](https://github.com/GRVYDEV/Project-Lightspeed)**  

  **Low-latency video relay and WebRTC live streaming server**, open-source . **OBS streaming backend that ingests media and converts for real-time browser playback** . **Sub-second delay between broadcast source and viewer** . **WebSocket stream orchestrator** for connection handshakes and signaling  . **Best for low-latency OBS-to-browser streaming** .



### Additional Strong Open-Source Options



- **RTPProxy** — General purpose high performance RTP proxy  .

- **RTP:Engine** — RTP and UDP based media traffic proxy, usable as kernel module  .

- **coturn** — TURN/STUN server for NAT traversal  .

- **eturnal** — Modern scalable STUN/TURN server in Erlang  .

- **ZLMediaKit** — High-performance C++ media server with RTSP, RTMP, HLS, WebRTC, GB28181  .

- **EasyDarwin** — Industrial RTSP streaming server with distributed load balancing  .

- **Restreamer** — Self-hosted multi-destination stream relay  .



**Frameworks for building custom live video transport solutions**: Combine **SRT** for low-latency contribution over lossy networks with AES encryption and ARQ . Use **RIST** for vendor-neutral reliable transport with SMPTE 2022-1 FEC and multicast/bonding support . Deploy **HydraSRT** for an open-source SRT gateway with failover and observability . Integrate **IRLServer** tooling for SRTLA bonding and OBS SRT/RIST sources . Use **ts-transformer** for sensor video with typed KLV metadata over SRT/RIST . Choose **MediaMTX** or **SRS** for multi-protocol media routing and protocol conversion . Note that true managed live video transport with global infrastructure, automatic scaling, and vendor-supported SLAs (AWS MediaConnect, Zixi, Haivision) remains primarily commercial territory; open-source stacks provide strong protocol implementations, gateway software, and media routing foundations that require integration for complete live video transport.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Live video transport handles broadcast-quality media and may process sensitive content. Self-hosted solutions require proper security hardening, bandwidth planning, and compliance with content regulations.

- **Protocol selection depends on requirements** — SRT for low-latency contribution with ARQ and encryption; RIST for vendor-neutral interoperability with FEC and bonding; Zixi for proprietary content-aware optimization with hitless redundancy . **Vendor interoperability is mandatory but not sufficient** — adaptive encoder rate control and output failover often remain vendor-implementation-dependent .

- **License considerations**: HydraSRT uses Apache-2.0 , SRT uses MPL-2.0, libRIST uses BSD-2-Clause , MediaMTX uses MIT , and ts-transformer is open-source . Verify licensing against your use case before committing.

- The open-source ecosystem provides strong protocol implementations, gateway software, and media routing foundations, but **global infrastructure, automatic scaling, and vendor-supported SLAs** remain primarily commercial offerings.



---



**Made for broadcast engineers, media transport specialists, and organizations seeking live video transport sovereignty.**

Let's make live video transport more open, transparent, and reliable.
