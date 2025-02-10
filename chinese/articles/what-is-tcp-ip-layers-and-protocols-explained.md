> * 原文：[TCP/IP 是什么？层和协议解释](https://www.freecodecamp.org/news/what-is-tcp-ip-layers-and-protocols-explained/)
> * 作者：Victoria Drake（维多利亚·德雷克）
> * 译者：Albert210（阿尔伯特210）
> * 校对者：

![TCP/IP是什么？层和协议解释](https://www.freecodecamp.org/news/content/images/size/w2000/2020/11/cover-2.png)

在创造某物的过程中，能够想象出尚未存在的事物是很重要的一部分。

这项技能对互联网的创建至关重要。如果没有人想象出这一大多数人现在每天视为理所当然的基础技术，就不会有猫meme的表情包出现。

为了使互联网成为可能，需要想象能力的两个东西是 _层_ 和 _协议_。

层是概念性的划分，意味着将相似的功能分组在一起。而协议这个词大致意味着我们在这里同意做事情的方式。

简而言之，可以将层和协议解释给一个五岁的孩子听，就像是，出现了人们认为听起来不错的主意，然后他们把这些主意写下来，这样其他人就可以用同样的主意来做事情了。

互联网协议套件按照层次结构和协议来描述。总体而言，该套件指的是使我们能够无尽滚动的通信协议。

它通常以其基础协议而闻名：传输控制协议（TCP）和互联网协议（IP）。这些协议一起被称为TCP/IP，它们描述了互联网上的数据是如何打包、寻址、发送和接收的。

这就是为什么互联网协议套件或TCP/IP是一个想象中的彩虹层蛋糕。

## **图层是虚构的**

如果你考虑一下彩虹层海绵蛋糕的一般性质，它主要是由柔软、入口即化的香草制成的。这种好处本身就是由鸡蛋、黄油、面粉和甜味剂等组成的。

![一片彩虹层蛋糕的卡通牌子，上面写着“；耶！免费蛋糕”](https://www.freecodecamp.org/news/content/images/2020/11/free-cake.png)

彩虹海绵蛋糕的一层和另一层没有太大区别。通常，层之间的唯一区别是食用色素和一点糖霜。仔细想想，从上到下都是小菜一碟。彩虹层之所以存在，是因为面包师认为它们应该存在。

与蛋糕配料类似，计算机网络环境中的层主要由协议、算法和配置组成，其中还夹杂着一些数据。

如果将计算机网络的许多功能分成组，那么谈论计算机网络会更容易，因此某些人提出了对层的描述，我们称之为网络模型。TCP/IP只是众多网络模型中的一种。从这个意义上说，层是概念，而不是事物。
其中一些人是互联网工程任务组（IETF）的成员。他们创造了  [RFC-1122][1]  出版物，讨论互联网的通信层。几乎一半，都是制定的标准：

> ……涵盖通信协议层：链路层、IP层和传输层; 它的伙伴  [RFC-1123][2]  涵盖了应用程序和支持协议。

RFC-1122和RFC-1123描述的每一层都封装了满足该层功能的协议。让我们看看这些通信层中的每一层，看看TCP和IP在这个互联网层蛋糕模型中究竟是如何堆叠的。

## **链路层协议**

![链接蛋糕层卡通](https://www.freecodecamp.org/news/content/images/2020/11/link.png)

这一[链路层][3]  是通信协议的最基本或最低级别的分类。它处理在同一本地网络上的主机之间发送信息，并将数据从更高层转换到物理层。

链路层中的协议描述了数据如何与传输介质交互，例如通过特定硬件发送的电子信号。与其他层不同，链路层协议取决于所使用的硬件。

## **互联网层协议**

在 [互联网层][4] 中的协议描述如何通过互联网发送和接收数据。该过程涉及将数据打包成数据包，寻址和传输数据包，以及接收传入的数据包。

![网络蛋糕层卡通](https://www.freecodecamp.org/news/content/images/2020/11/internet.png)

这一层中最广为人知的协议赋予TCP/IP最后两个字母。IP是一种无连接协议，这意味着它不能保证数据包按照正确的顺序、沿着相同的路径甚至完整地发送或接收。

可靠性由套件中的其他协议处理，例如在传输层。

目前使用的IP有两个版本：IPv4和IPv6。这两个版本都描述了如何为互联网上的设备分配IP地址，这些地址在导航到猫模因时使用。

IPv4的使用更为广泛，但只有 [32 bits for addressing][5], 允许大约43亿（约4.3×109）个可能的地址。这些正在耗尽，随着越来越多的人在互联网上使用更多的设备，IPv4最终将遭受地址耗尽。

后续版本IPv6旨在通过 [using 128 bits for addresses][6]的方式解决网址耗尽问题。This provides, um,这提供了，嗯，更多地址的可能性。(ca. 3.4×1038)

## **传输层协议**

1974年5月，温特·瑟夫和鲍勃·卡恩（共同称为“互联网之父”）发表了一篇题为[一种分组网络互通协议][7]的文章。

本文首次描述了传输控制程序，这一概念涵盖了最终被称为传输控制协议（TCP）和用户数据报协议（UDP）的内容。(我很高兴见到温特，我可以亲自确认，是的，他看起来确实很像《黑客帝国》电影中的建筑师。)

![Transport cake layer cartoon](https://www.freecodecamp.org/news/content/images/2020/11/transport.png)

The  [transport layer][8]  presently encapsulates TCP and UDP. Like IP, UDP is connectionless and can be used to prioritize time over reliability.

TCP, on the other hand, is a connection-oriented transport layer protocol that prioritizes reliability over latency, or time. TCP describes transferring data in the same order as it was sent, retransmitting lost packets, and controls affecting the rate of data transmission.

## **Application layer protocols**

![Application cake layer cartoon](https://www.freecodecamp.org/news/content/images/2020/11/application.png)

The application layer describes the protocols that software applications interact with most often. The specification includes descriptions of the remote login protocol  [Telnet][9], the  [File Transfer Protocol (FTP)][10], and the  [Simple Mail Transfer Protocol (SMTP)][11].

Also included in the application layer are the Hypertext Transfer Protocol (HTTP) and its successor, Hypertext Transfer Protocol Secure (HTTPS).

HTTPS is secured by Transport Layer Security, or TLS, which can be said to be the top-most layer of the networking model described by the Internet protocol suite.

If you’d like to further understand TLS and how this protocol secures your cat meme viewing, I invite you  [read my article about TLS and cryptography][12].

## **The Internet cake is still baking**

Like a still-rising sponge cake, descriptions of layers, better protocols, and new models are being developed every day. The Internet, or whatever it will become in the future, is still in the process of being imagined.

![Cartoon of the full Internet layer cake, topped with Nyan Cat memes](https://www.freecodecamp.org/news/content/images/2020/11/cake.png)

If you enjoyed learning from this post, there’s a lot more where this came from! I write about computing, cybersecurity, and building great technical teams. Join the thousands of people who learn from my articles on  [victoria.dev][13]! Visit and subscribe by email or RSS to see new articles first.

[1]: https://tools.ietf.org/html/rfc1122
[2]: https://tools.ietf.org/html/rfc1123
[3]: https://tools.ietf.org/html/rfc1122#page-21
[4]: https://tools.ietf.org/html/rfc1122#page-27
[5]: https://tools.ietf.org/html/rfc791#section-2.3
[6]: https://tools.ietf.org/html/rfc8200#section-1
[7]: https://web.archive.org/web/20160304150203/http://ece.ut.ac.ir/Classpages/F84/PrincipleofNetworkDesign/Papers/CK74.pdf
[8]: https://tools.ietf.org/html/rfc1122#page-77
[9]: https://tools.ietf.org/html/rfc1123#section-3
[10]: https://tools.ietf.org/html/rfc1123#section-4
[11]: https://tools.ietf.org/html/rfc1123#section-5
[12]: https://victoria.dev/blog/tls
[13]: https://victoria.dev/
