# Unexpected Messages
# 不可预料的消息
Messages you didn’t know about tend to be rather rare when using OTP applications.<br>
Because OTP behaviours pretty much expect you to handle anything with some clause in handle_info /2, unexpected messages will not accumulate much.<br>
However, all kinds of OTP-compliant systems end up having processes that may not implement a behaviour, or processes that go in a non-behaviour stretch where it overtakes message handling.<br>
If you’re lucky enough, monitoring tools <sup>6</sup> will show a constant memory increase, and inspecting for large queue sizes <sup>7</sup> will let you find which process is at fault.<br>
You can then fix the problem by handling the messages as required.
<p></p> <font color="green">
&emsp;OTP applications里面几乎不存在出乎意料的消息。
因为OTP behaviours 会用handle_info/2来处理所有的消息，所以基本不会堆积很多不明的消息。<br>
&emsp;然而，并不是所有服从OTP的系统都会实现behaviour的中指定的函数(编：如handle_info/2)，或不符合behaviour的进程没有做好(overtakes)消息处理.<br>
&emsp;如果你足够幸运，监控工具<sup>6</sup>会监测到噌噌往上涨的内存，你可以通过检查大型队列<sup>7</sup>来找出哪个进程出错了。<br>
&emsp;那么你按需求处理好这些消息（没有被处理的）就可以修复问题啦。
</font> <p></p>

[6] See Section 5.1 <br>
[7] See Subsection 5.2.1 <br>
<p></p> <font color="green">

[注6]：见5.1<br>
[注7]：见5.2.1
</font> <p></p>
