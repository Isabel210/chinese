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

> ……covers the communications protocol layers: link layer, IP layer, and transport layer; its companion  [RFC-1123][2]  covers the application and support protocols.

The layers described by RFC-1122 and RFC-1123 each encapsulate protocols that satisfy the layer’s functionality. Let’s look at each of these communications layers and see how TCP and IP stack up in this model of the Internet layer cake.

## **Link layer protocols**

![Link cake layer cartoon](https://www.freecodecamp.org/news/content/images/2020/11/link.png)

The  [link layer][3]  is the most basic, or lowest-level, classification of communication protocol. It deals with sending information between hosts on the same local network, and translating data from the higher layers to the physical layer.

Protocols in the link layer describe how data interacts with the transmission medium, such as electronic signals sent over specific hardware. Unlike other layers, link layer protocols are dependent on the hardware being used.

## **Internet layer protocols**

Protocols in the  [Internet layer][4]  describe how data is sent and received over the Internet. The process involves packaging data into packets, addressing and transmitting packets, and receiving incoming packets of data.

![Internet cake layer cartoon](https://www.freecodecamp.org/news/content/images/2020/11/internet.png)

The most widely known protocol in this layer gives TCP/IP its last two letters. IP is a connectionless protocol, meaning that it provides no guarantee that packets are sent or received in the right order, along the same path, or even in their entirety.

Reliability is handled by other protocols in the suite, such as in the transport layer.

There are currently two versions of IP in use: IPv4, and IPv6. Both versions describe how devices on the Internet are assigned IP addresses, which are used when navigating to cat memes.

IPv4 is more widely used, but has only  [32 bits for addressing][5], allowing for about 4.3 billion (ca. 4.3×109) possible addresses. These are running out, and IPv4 will eventually suffer from address exhaustion as more and more people use more devices on the Internet.

The successor version IPv6 aims to solve address exhaustion by  [using 128 bits for addresses][6]. This provides, um, a  _lot_  more address possibilities (ca. 3.4×1038).

## **Transport layer protocols**

In May 1974, Vint Cerf and Bob Kahn (collectively often called “the fathers of the Internet”) published a paper entitled  [A Protocol for Packet Network Intercommunication][7].

This paper contained the first description of a Transmission Control Program, a concept encompassing what would eventually be known as the Transmission Control Protocol (TCP) and User Datagram Protocol (UDP). (I had the pleasure of meeting Vint and can personally confirm that yes, he does look exactly like The Architect in the Matrix movies.)

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
