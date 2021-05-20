            <div class="article" id="con">
                <div class="section">
                    <div class="page-header" id="win-terminal"><span></span>Win8/Win7/Vista</div>
                        <ol>
                       
                            <li>

                                <p>在电脑右下角的网络图标上单击鼠标右键可以看到"打开网络和共享中心"选项，点击进入设置</p>
                                <div class="setting-img"><img src="https://796668.com/img/settings/win8-setting-0.jpg" alt="打开网络和共享中心"></div>
                            </li>
                            <li>
                                <p>点击左侧的"更改适配器设置"</p>
                                <div class="setting-img"><img src="#" _src="img/settings/win8-setting-1.jpg" alt="更改适配器设置"></div>
                            </li>
                            <li>
                                <p>在选中的网络连接上单击鼠标右键，选择"属性"</p>
                                <div class="setting-img"><img src="#" _src="img/settings/win8-setting-2.jpg" alt="网络连接"></div>
                            </li>
    
    
                            <li>
                                <p>单击"网络"选项卡。在"此连接使用下列项目"下，选中"Internet 协议版本 4 (TCP/IPv4)"，然后点击"属性"，或者直接双击"Internet 协议版本 4 (TCP/IPv4)"</p>
                                <div class="setting-img"><img src="#" _src="img/settings/win8-setting-3.jpg" alt="WLAN属性"></div>
                            </li>
                            <li>
                                <p>勾选"使用下面的DNS服务地址"，然后在"首选DNS服务器"和"备用DNS服务器"框中，键入主DNS服务器地址180.76.76.76和辅助DNS服务器的地址114.114.114.114，点击确定即设置完成</p>
                                <div class="setting-img"><img src="#" _src="img/settings/win8-setting-4.jpg" alt="域名设定"></div>
                            </li>
                        </ol>
                        <div class="page-header" id="linux-terminal"><span></span>Linux 系统</div>
                        <ol>
                            <li>
                                <p>以下设置对所用的Linux系统如Redhat/Ubuntu/Debian/CentOS等都有效，但您必须是管理员root或者具有管理员权限</p>
                                <pre>vim /etc/resolv.conf</pre>
                            </li>
                            <li>
                                <p>在其中加入:</p>
                                <pre>nameserver 180.76.76.76<br>nameserver 114.114.114.114</pre>
                            </li>
                            <li>
                                <p>保存退出,使用nslookup或者dig验证是否可以通过180.76.76.76正常解析www.baidu.com</p>
                            </li>
                        </ol>
                        <div class="page-header" id="mac-terminal"><span></span>Mac系统</div>
                        <ol>
                            <li>
                                <p>单击最左上角的苹果图标，在下拉菜单中点击"系统偏好设置"进入设置</p>
                                <div class="setting-img"><img src="#" _src="img/settings/Mac-setting-0.png" alt="Mac系统-系统偏好设置"></div>
                            </li>
                            <li>
                                <p>单击"网络"图标进入网络设置</p>
                                <div class="setting-img"><img src="#" _src="img/settings/Mac-setting-1.png" alt="Mac系统-网络设置"></div>
                            </li>
                            <li>
                                <p>从列表中选择相应的网络连接服务，然后单击"高级"选项</p>
                                <div class="setting-img"><img src="#" _src="img/settings/Mac-setting-2.png" alt="Mac系统-网络连接服务"></div>
                            </li>
                            <li>
                                <p>点击DNS的选项卡，然后点击左下角"+"，添加180.76.76.76和114.114.114.114，单击"好"</p>
                                <div class="setting-img"><img src="#" _src="img/settings/Mac-setting-3.png" alt="Mac系统-DNS服务器"></div>
                            </li>
                            <li>
                                <p>返回到上一级，单击"应用"</p>
                            </li>
                            <li>
                                <p>在浏览器中测试打开 http://www.baidu.com是否正常</p>
                            </li>
                        </ol>
                </div>
    
                <div class="section">
                    <div class="page-header" id="ios-mobile"><span></span>IOS</div>
                    <ol>
                        <li>
                            <p>在主屏幕中点击"设置"图标进入设置界面</p>
                        </li>
                        <li>
                            <p>点击"无线局域网"</p>
                            <div class="setting-img"><img src="#" _src="img/settings/phone-setting-0.png" alt="IOS-无线局域网"></div>
                        </li>
                        <li>
                            <p>在"选取网络"列表中点击相应的网络链接右侧的"i"图标，进入网络设置</p>
                            <div class="setting-img"><img src="#" _src="img/settings/phone-setting-1.png" alt="IOS-无线局域网"></div>
                        </li>
                        <li>
                            <p>选择"DHCP"选项卡，设置选项下的"DNS"为180.76.76.76, 114.114.114.114即可</p>
                            <div class="setting-img"><img src="#" _src="img/settings/phone-setting-2.png" alt="IOS-域名设置"></div>
                        </li>
                    </ol>
                    <div class="page-header" id="android-mobile"><span></span>Android</div>
                    <ol>
                        <li>
                            <p>在桌面点击"设置"图标，并且进入"WLAN设置"选项</p>
                            <div class="setting-img"><img src="#" _src="img/settings/Android-setting-0.jpg" alt="Android-Wlan设置"></div>
                        </li>
                        <li>
                            <p>在wifi列表中，选择已经连接的WiFi网络，长按之后在弹出来的提示选择"修改网络"</p>
                            <div class="setting-img"><img src="#" _src="img/settings/Android-setting-1.jpg" alt="Android-修改网络"></div>
                        </li>
                        <li>
                            <p>选中"显示高级选项"，将"IP设定"改成"静止"</p>
                            <div class="setting-img"><img src="#" _src="img/settings/Android-setting-2.jpg" alt="Android-IP设定"></div>
                        </li>
                        <li>
                            <p>将域名1和域名2分别改成180.76.76.76和114.114.114.114，保存即可</p>
                            <div class="setting-img"><img src="#" _src="img/settings/Android-setting-3.jpg" alt="Android-域名设定"></div>
                        </li>
                    </ol>
                </div>
    
                <div class="section">
                    <div class="page-header" id="mi-router"><span></span>小米路由</div>
                    <ol>
                        <li>
                            <p>在界面中点击"路由设置"进入设置界面</p>
                        </li>
                        <li>
                            <p>在右边栏的网络设置展开菜单选中"外网设置"进入设置</p>
                            <div class="setting-img"><img src="#" _src="img/settings/mi-setting-0.jpg" alt="小米路由-路由设置"></div>
                        </li>
                        <li>
                            <p>在右边界面"配置联网类型"选择"使用静态IP"，设置选项下的"DNS1"为180.76.76.76, "DNS2"为114.114.114.114</p>
                            <div class="setting-img"><img src="#" _src="img/settings/mi-setting-1.jpg" alt="小米路由-外网设置"></div>
                        </li>
                    </ol>
                    <div class="page-header" id="jk-router"><span></span>极路由</div>
                    <ol>
                        <li>
                            <p>登陆路由器，点击左下角外网设置</p>
                            <div class="setting-img"><img src="#" _src="img/settings/router-setting-0.jpg" alt="极路由-外网设置"></div>
                        </li>
                        <li>
                            <p>根据上网方式选择宽带拨号或网线接入（多为宽带拨号），勾选"自定义DNS"，然后在DNS地址输入框中分别输入180.76.76.76和114.114.114.114，点击保存完成设置</p>
                            <div class="setting-img"><img src="#" _src="img/settings/router-setting-1.jpg" alt="极路由-域名设定"></div>
                        </li>
                    </ol>
                    <div class="page-header" id="other-router"><span></span>其他</div>
                    <ol>
                        <li>
                            <p>登录路由器管理界面，找到外网设置（不同厂商的可能名称不太一样）相关选项卡。</p>
                        </li>
                        <li>
                            <p>找到DNS配置区域，设置首选DNS地址180.76.76.76，备选114.114.114.114。</p>
                        </li>
                        <li>
                            <p>如有任何疑问，请直接联系我们。</p>
                        </li>
                    </ol>
                    
                </div>
            </div>
