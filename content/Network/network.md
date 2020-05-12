# NETWORK

[![HOME](../../img/button_home.png)](https://github.com/mmmarceleza/My-Learning-Tracker#marcelos-learning-tracker) &nbsp; &nbsp; [![MY ARTICLES](../../img/button_article.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/my-articles.md#my-articles) &nbsp; &nbsp; [![PORTFOLIO](../../img/button_portfolio.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/portfolio.md#portfolio) &nbsp; &nbsp; [![LEARNING LOG](../../img/button_log.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/learning-log.md#learning-log)

***
## Completed Courses:

|   | Courses | Certificate |
|:---:|:---:|:---:|
| ![Redes](../../img/redes-introducao.png) | [Redes parte 1: Introdução, Conceitos e Prática](https://cursos.alura.com.br/course/redes-introducao) | [Certificate](https://cursos.alura.com.br/certificate/84acbdd7-ec2d-427a-bd54-0ecfb4d092e9) |

***

## My notes

## Classes of IP addresses

### Classes

| **Class** | **Leading bits** | **Number of networks** | **Addresses per network** | **Start address** | **End address** | **Default subnet mask** |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Class A | 0 | 128 | 16,777,216 | 0.0.0.0 | 127.255.255.255 | 255.0.0.0 | 
| Class B | 10 | 16,384 | 65,536 | 128.0.0.0 | 191.255.255.255 | 255.255.0.0 |
| Class C | 110 | 2,097,152 | 256 | 192.0.0.0 | 223.255.255.255 | 255.255.255.0 |
| Class D | 1110 | not defined | not defined | 224.0.0.0 | 239.255.255.255 | not defined |
| Class E | 1111 | not defined | not defined | 240.0.0.0 | 255.255.255.255 | not defined |

Class D is reserved for multicast and cannot be used for regular unicast traffic. Class E is reserved and cannot be used on the public Internet.

### Bit-wise representation

In the following bit-wise representation,

- n indicates a bit used for the network ID.
- H indicates a bit used for the host ID.
- X indicates a bit without a specified purpose.

```
Class A
  0.  0.  0.  0 = 00000000.00000000.00000000.00000000
127.255.255.255 = 01111111.11111111.11111111.11111111
                  0nnnnnnn.HHHHHHHH.HHHHHHHH.HHHHHHHH

Class B
128.  0.  0.  0 = 10000000.00000000.00000000.00000000
191.255.255.255 = 10111111.11111111.11111111.11111111
                  10nnnnnn.nnnnnnnn.HHHHHHHH.HHHHHHHH

Class C
192.  0.  0.  0 = 11000000.00000000.00000000.00000000
223.255.255.255 = 11011111.11111111.11111111.11111111
                  110nnnnn.nnnnnnnn.nnnnnnnn.HHHHHHHH

Class D
224.  0.  0.  0 = 11100000.00000000.00000000.00000000
239.255.255.255 = 11101111.11111111.11111111.11111111
                  1110XXXX.XXXXXXXX.XXXXXXXX.XXXXXXXX

Class E
240.  0.  0.  0 = 11110000.00000000.00000000.00000000
255.255.255.255 = 11111111.11111111.11111111.11111111
                  1111XXXX.XXXXXXXX.XXXXXXXX.XXXXXXXX
```

### Private IP addresses

This ranges of IP are used in private networks and they are not unique. To access the internet It's necessary to use a router and a technology called Network Address Translation (NAT). Each class has your range, as seen below:

- Class A
    - 10.0.0.0 – 10.255.255.255
- Class B
    - 172.16.0.0 – 172.31.255.255
- Class C
    - 192.168.0.0 – 192.168.255.255

