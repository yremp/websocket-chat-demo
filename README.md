<!-- wp:paragraph -->
<p>Spring Boot+WebSocket实现多人在线聊天室 ，简单的给大家分享一下这个项目。项目很简单，不用数据库就可以实现多人在线聊天。刚刚学习Spring Boot 和WebSocekt的话可以参考这一下这个项目，也可以进行二次开发。</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>前言</h3>
<!-- /wp:heading -->

<!-- wp:list {"ordered":true} -->
<ol><li><a href="https://spring-ws-chat.herokuapp.com/">在线演示地址</a></li><li><a href="https://github.com/yremp/websocket-chat-demo">我的项目地址 </a></li><li>此项目源码来源于老外的项目，<a href="https://www.callicoder.com/spring-boot-websocket-chat-example/">原文地址</a> | <a href="https://github.com/callicoder/spring-boot-websocket-chat-demo">项目地址</a></li><li>参考了简书上面一篇相关文章：<a href="https://www.jianshu.com/p/b3dd8a1b7e72">原文地址</a> | <a href="https://github.com/qqxx6661/springboot-websocket-demo">项目地址</a></li></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>我的基本上和原作者项目保持一致，简书上面的项目 博主已经进行了集群开发，下载后需要配置一些东西可能才能体验，我的下载后可以直接运行，如果想快速上手可以下载我的项目。</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>项目预览</h3>
<!-- /wp:heading -->

<!-- wp:heading {"level":4} -->
<h4>

设置名称

</h4>
<!-- /wp:heading -->

<!-- wp:image {"id":1536} -->
<figure class="wp-block-image"><img src="https://yremp.live/wp-content/uploads/2019/09/image-22-1024x521.png" alt="" class="wp-image-1536"/></figure>
<!-- /wp:image -->

<!-- wp:heading {"level":4} -->
<h4>聊天</h4>
<!-- /wp:heading -->

<!-- wp:image {"id":1538} -->
<figure class="wp-block-image"><img src="https://yremp.live/wp-content/uploads/2019/09/image-24-1024x521.png" alt="" class="wp-image-1538"/></figure>
<!-- /wp:image -->

<!-- wp:heading {"level":3} -->
<h3>项目结构</h3>
<!-- /wp:heading -->

<!-- wp:list {"ordered":true} -->
<ol><li>websocket<ul><li>controller<ul><li>ChatController.class</li></ul></li><li>entity<ul><li>ChatMessage.class</li></ul></li><li>listener<ul><li>WebSocketEventListener.class</li></ul></li><li>WebSocketConfig<ul><li> WebSocketConfig .class</li></ul></li></ul></li><li>resource<ul><li>static<ul><li>css<ul><li>main.css</li></ul></li><li>js<ul><li>main.js</li></ul></li></ul></li><li>templates<ul><li>index.html</li></ul></li></ul></li></ol>
<!-- /wp:list -->

<!-- wp:heading {"level":3} -->
<h3>项目说明</h3>
<!-- /wp:heading -->

<!-- wp:heading {"level":4} -->
<h4>1.引入websocket依赖</h4>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;dependency>
            &lt;groupId>org.springframework.boot&lt;/groupId>
            &lt;artifactId>spring-boot-starter-websocket&lt;/artifactId>
        &lt;/dependency></code></pre>
<!-- /wp:code -->

<!-- wp:heading {"level":4} -->
<h4>2.项目文件说明</h4>
<!-- /wp:heading -->

<!-- wp:list {"ordered":true} -->
<ol><li> WebSocketConfig.class              -配置类</li><li>ChatMessage.class                       -消息实体类</li><li>CahtController.class                    -控制器</li><li>WebSocketEventListen.class     -事件监听 </li><li>static以及templates                     -静态文件资源</li></ol>
<!-- /wp:list -->

<!-- wp:heading {"level":3} -->
