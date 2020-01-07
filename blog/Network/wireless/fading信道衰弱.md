## 无线网络通讯的Fading
[TOC]

![d670253c0be0c6be223a597b4f4546d7.gif](evernotecid://A1FFF222-EE60-4C12-8ADC-6214C169308F/wwwevernotecom/147639754/ENResource/p4023)

由于无线信号传播中可能经历反射、衍射和散射三个过程， 接收信号一般地讲是一个多径信号。 随着发射机和接收机距离的增大， 接收信号的损耗是十分明显的。

* * *
### Large-scale

>Large-scale fading is the result of signal attenuation due to signal propagation over large distances and diffraction around large objects in the propagation path.

Large-scale fading 是由于长距离传输导致的信号衰弱。 预测信号**平均值**下降的模型叫做Large-Scale 模型（大尺度衰落）。
影响Large-scale fading的两个元素包括：
#### Relative Path Loss (loss due to distance)

>In free-space, the attenuation of a signal due to distance follows the $1/d^2$ law, where $d$ is the distance between the transmitter and the receiver. This is the case for line-of-sight (LOS) signals (path B). In the case of non-line-of-sight (NLOS) signals (path A), the attenuation is more likely to be anywhere from $1/d^3$ to $1/d^6$. This additional loss of power in propagation channels occurs when part of the reflected signal is lost.

Large-scale fadin与路径损耗（Path Loss）有关（取决于距离），LOS和NLOS的丢包率也不一样。

#### Shadowing
>Log-normal shadowing is the result of the signal being blocked by large objects in the propagation path (path D). These are typically distant objects in the environment such as mountains, hills, or large buildings. The length of time it takes for a moving receiver to pass through the "shadow" of these obstacles brings about the term "slow fading". The statistical model used to describe shadowing is the log-normal distribution of the mean signal power.
>
阴影

* * *
### Small-scale

由于**多径信号相干叠加引起**的衰落称之为Small-Scale模型（小尺度衰落），其预测模型称为Small-Scale模型。
下面是3种不同的模型。
#### [Rayleigh Fading](https://zh.wikipedia.org/wiki/%E7%91%9E%E5%88%A9%E8%A1%B0%E8%90%BD%E4%BF%A1%E9%81%93)
>Rayleigh fading is used to simulate the rapid amplitude fluctuations where there is no direct ray component. Because there is no direct ray component, Rayleigh fading is often classified as the worst case fading type. Using a one ray model, this small scale distribution simulates the effects of rapid amplitude fluctuations when the receiver travels a distance of a few wavelengths. The one ray is scattered near the receiver resulting in a large number of rays arriving at the receiver from all directions (path C). The signals add in and out of phase giving rise to amplitude fluctuations that vary at a rate that is dependent on the speed of the receiver. The statistical model used to describe the amplitude variations is the Rayleigh probability distribution function. The receiver movement also produces a spreading of the signal in the frequency domain due to the Doppler effect.

Rayleigh衰落用于模拟没有**直接射线**成分的快速幅度波动。
瑞利衰落只适用于从发射机到接收机不存在直射信号（LoS，Line of Sight）的情况，否则应使用莱斯衰落信道（Rician fading channel）作为信道模型。