# centos7-shadowsock
1安装shadowsocks：逐条输入</br>
1.输入  wget --no-check-certificate -O shadowsocks.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks.sh 


2.输入   chmod +x shadowsocks.sh</br>
3.输入      ./shadowsocks.sh 2>&1 | tee shadowsocks.log</br>
2 添加端口到防火墙：
比如开放8989端口</br>
2.1<code>firewall-cmd --permanent --add-port=8989/tcp</code>
载入新的防火墙端口设置</br>
2.2<code>firewall-cmd --reload</code></br>
单个配置文件路径：/etc/shadowsocks.json 修改文件用vi /etc/shadowsocks.json 然后输入:wq 保存
<link rel='stylesheet' type='text/css' href='http://tools.oschina.net/js/syntaxhighlighter_3.0.83/styles/shCoreDjango.css'/><div id="highlighter_449060" class="syntaxhighlighter  js"><div class="toolbar"><span><a href="#" class="toolbar_item command_help help">?</a></span></div><table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="js plain">{</code></div><div class="line number2 index1 alt1"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"server"</code><code class="js plain">:</code><code class="js string">"0.0.0.0"</code><code class="js plain">,</code></div><div class="line number3 index2 alt2"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"server_port"</code><code class="js plain">:8989,</code></div><div class="line number4 index3 alt1"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"local_address"</code><code class="js plain">:</code><code class="js string">"127.0.0.1"</code><code class="js plain">,</code></div><div class="line number5 index4 alt2"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"local_port"</code><code class="js plain">:1080,</code></div><div class="line number6 index5 alt1"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"password"</code><code class="js plain">:</code><code class="js string">"yourpassword"</code><code class="js plain">,</code></div><div class="line number7 index6 alt2"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"timeout"</code><code class="js plain">:300,</code></div><div class="line number8 index7 alt1"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"method"</code><code class="js plain">:</code><code class="js string">"aes-256-cfb"</code><code class="js plain">,</code></div><div class="line number9 index8 alt2"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"fast_open"</code><code class="js plain">:&nbsp;</code><code class="js keyword">false</code></div><div class="line number10 index9 alt1"><code class="js plain">}</code></div></div></td></tr></tbody></table></div>
</br>
多个个配置文件路径：/etc/shadowsocks.json 修改文件用vi /etc/shadowsocks.json 然后输入:wq 保存</br>
<link rel='stylesheet' type='text/css' href='http://tools.oschina.net/js/syntaxhighlighter_3.0.83/styles/shCoreDjango.css'/><div id="highlighter_347772" class="syntaxhighlighter  js"><div class="toolbar"><span><a href="#" class="toolbar_item command_help help">?</a></span></div><table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div><div class="line number12 index11 alt1">12</div><div class="line number13 index12 alt2">13</div><div class="line number14 index13 alt1">14</div><div class="line number15 index14 alt2">15</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="js plain">{</code></div><div class="line number2 index1 alt1"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"server"</code><code class="js plain">:</code><code class="js string">"0.0.0.0"</code><code class="js plain">,</code></div><div class="line number3 index2 alt2"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"local_address"</code><code class="js plain">:</code><code class="js string">"127.0.0.1"</code><code class="js plain">,</code></div><div class="line number4 index3 alt1"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"local_port"</code><code class="js plain">:1080,</code></div><div class="line number5 index4 alt2"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"port_password"</code><code class="js plain">:{</code></div><div class="line number6 index5 alt1"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"8989"</code><code class="js plain">:</code><code class="js string">"password0"</code><code class="js plain">,</code></div><div class="line number7 index6 alt2"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"9001"</code><code class="js plain">:</code><code class="js string">"password1"</code><code class="js plain">,</code></div><div class="line number8 index7 alt1"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"9002"</code><code class="js plain">:</code><code class="js string">"password2"</code><code class="js plain">,</code></div><div class="line number9 index8 alt2"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"9003"</code><code class="js plain">:</code><code class="js string">"password3"</code><code class="js plain">,</code></div><div class="line number10 index9 alt1"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"9004"</code><code class="js plain">:</code><code class="js string">"password4"</code></div><div class="line number11 index10 alt2"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js plain">},</code></div><div class="line number12 index11 alt1"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"timeout"</code><code class="js plain">:300,</code></div><div class="line number13 index12 alt2"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"method"</code><code class="js plain">:</code><code class="js string">"aes-256-cfb"</code><code class="js plain">,</code></div><div class="line number14 index13 alt1"><code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js string">"fast_open"</code><code class="js plain">:&nbsp;</code><code class="js keyword">false</code></div><div class="line number15 index14 alt2"><code class="js plain">}</code></div></div></td></tr></tbody></table></div></br>
使用命令
</br><link rel='stylesheet' type='text/css' href='http://tools.oschina.net/js/syntaxhighlighter_3.0.83/styles/shCoreDjango.css'/><div id="highlighter_969916" class="syntaxhighlighter  js"><div class="toolbar"><span><a href="#" class="toolbar_item command_help help">?</a></span></div><table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="js plain">启动：/etc/init.d/shadowsocks&nbsp;start</code></div><div class="line number2 index1 alt1"><code class="js plain">停止：/etc/init.d/shadowsocks&nbsp;stop</code></div><div class="line number3 index2 alt2"><code class="js plain">重启：/etc/init.d/shadowsocks&nbsp;restart</code></div><div class="line number4 index3 alt1"><code class="js plain">状态：/etc/init.d/shadowsocks&nbsp;status</code></div></div></td></tr></tbody></table></div>
这些端口是我转载的，可以确定的是大部分端口有效可免流。

移动免流端口：137,138,351,366,265,524,8080,80,443,440,3389

电信免流端口：189,8080,80,443,440,3389,137

联通免流端口：8080,80,53(空中卡),130,131,132,155,156,185,186,145,176,443,440,3389

部分端口也未经测试，请自行测试。
除了部分端口直连能免，大部分都需要加混肴参数 

SSR免流可以用，440/443应该是op免流也能用，在搭建的SSR免流的时候选择自己常用的运营商，然后选择对应的端口进行搭建就行。
