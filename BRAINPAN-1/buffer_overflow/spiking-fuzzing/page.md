::: page
# Spiking/Fuzzing {#spikingfuzzing .title}

\

We ran brainpan.exe on windows :

![](104-1.png)

Says listening on **port 9999**.

We **netcat** to that port :

![](104-2.png)

It is asking us for a **password**.

Lets generate a **large string of "A"** and **pass this as a password**
to see how the chat application responses :

![](104-3.png)

We got this **error** :

![](104-4.png)

This confirms we can **overflow the buffer**.

Lets check the **immunity debugger** output :

![](104-5.png)

Here, we can see that **EIP can be controlled** and hence we can
**overflow the buffer to execute out patload and get root.**
:::
