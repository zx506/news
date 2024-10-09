<script setup>
import { ref, computed } from 'vue';
import { onMounted } from 'vue'; // 确保 onMounted 被导入
import 'animate.css'; // 引入 animate.css
import { Search } from '@element-plus/icons-vue'
import gasp  from 'gsap';
// 在组件挂载后开始旋转动画
onMounted(() => {
  // 创建时间线并设置无限循环和来回播放
  const tl = gasp.timeline({ repeat: -1});

  // 第一次旋转 180 度
  tl.to("#rotating-ai-assistant", {
    rotation: 180, // 旋转180度
    duration: 1, // 持续1秒
    ease: "power1.out" // 缓动效果
  })
  // 等待 1 秒
  .to({}, { duration: 1 })
  // 再旋转 180 度，总共旋转 360 度
  .to("#rotating-ai-assistant", {
    rotation: 360, // 再旋转180度
    duration: 1, // 持续1秒
    ease: "power1.out" // 缓动效果
  })
  // 等待 1 秒
  .to({}, { duration: 1 });
})
const newsList1 = ref([
  { id: 1, title: '一波减持预告来了：格力电器也要卖1242万股', content: '今日（10月8日）为节后第一个交易日，A股市场大幅高开，三大指数...' 
  , image: "/news1.jfif"},
  { id: 2, title: '马克龙呼吁对以色列全面武器禁运 英国国防大臣拒绝', content: '针对法国总统马克龙此前提出的西方国家...' 
  , image: "/news2.jfif"},
  { id: 3, title: '刚刚！诺贝尔物理学奖颁给了两位AI科学家', content: '刚刚， 2024年诺贝尔物理学奖公布。约翰·霍普菲尔...' 
  , image: "/news3.jfif"},
  { id: 1, title: '蔡英文被指将于本月访问捷克 外交部回应', content: '应东盟轮值主席国老挝人民民主共和国总理宋赛邀请...' 
  , image: "/news4.jfif"},
  { id: 2, title: '伊涅斯塔：可能是最懂怎么踢足球的人', content: '伊涅斯塔要退役了，40岁。...' 
  , image: "/news5.jfif"},
  { id: 3, title: '上海最年轻区委书记调任 成江苏最年轻地级市市委书记', content: '最新消息，江苏省委决定：姜冬冬同志...' 
  , image: "/news6.jfif"},
  { id: 1, title: '中共中央 全国人大常委会 国务院 全国政协讣告 吴邦国同志逝世', content: '新华社北京10月8日电 中国共产党中央委...' 
  , image: "/news7.jfif"},
  { id: 2, title: '光影“魔法”！带你一起解锁“夜上海”新玩法', content: '从上海展览中心到浦江两岸从建筑投影秀到光影艺术...' 
  , image: "/news8.jfif"},
  { id: 3, title: '国庆小长假补觉记得要保持规律性', content: '国庆假期除了出游，没有了上班时间的“限制”，好好补觉...' 
  , image: "/news9.jfif"}
])
const newsList2 = ref([
  { id: 1, title: '蔡英文被指将于本月访问捷克 外交部回应', content: '应东盟轮值主席国老挝人民民主共和国总理宋赛邀请...' 
  , image: "/news4.jfif"},
  { id: 2, title: '伊涅斯塔：可能是最懂怎么踢足球的人', content: '伊涅斯塔要退役了，40岁。...' 
  , image: "/news5.jfif"},
  { id: 3, title: '上海最年轻区委书记调任 成江苏最年轻地级市市委书记', content: '最新消息，江苏省委决定：姜冬冬同志...' 
  , image: "/news6.jfif"},
  { id: 1, title: '中共中央 全国人大常委会 国务院 全国政协讣告 吴邦国同志逝世', content: '新华社北京10月8日电 中国共产党中央委...' 
  , image: "/news7.jfif"},
  { id: 2, title: '光影“魔法”！带你一起解锁“夜上海”新玩法', content: '从上海展览中心到浦江两岸从建筑投影秀到光影艺术...' 
  , image: "/news8.jfif"},
  { id: 3, title: '国庆小长假补觉记得要保持规律性', content: '国庆假期除了出游，没有了上班时间的“限制”，好好补觉...' 
  , image: "/news9.jfif"}
])
const newsList3 = ref([
  { id: 1, title: '中共中央 全国政协讣告 吴邦国同志逝世', content: '新华社北京10月8日电 中国共产党中央委...' 
  , image: "/news7.jfif"},
  { id: 2, title: '光影“魔法”！带你一起解锁“夜上海”新玩法', content: '从上海展览中心到浦江两岸从建筑投影秀到光影艺术...' 
  , image: "/news8.jfif"},
  { id: 3, title: '国庆小长假补觉记得要保持规律性', content: '国庆假期除了出游，没有了上班时间的“限制”，好好补觉...' 
  , image: "/news9.jfif"}
])
const newsList4 = ref([
  { id: 3, title: '刚刚！诺贝尔物理学奖颁给了两位AI科学家', content: '刚刚， 2024年诺贝尔物理学奖公布。约翰·霍普菲尔...' 
  , image: "/news3.jfif"},
  { id: 3, title: '上海最年轻区委书记调任 成江苏最年轻地级市市委书记', content: '最新消息，江苏省委决定：姜冬冬同志...' 
  , image: "/news6.jfif"},
  { id: 3, title: '国庆小长假补觉记得要保持规律性', content: '国庆假期除了出游，没有了上班时间的“限制”，好好补觉...' 
  , image: "/news9.jfif"}
])
// 定义一个变量来控制按钮的禁用状态
const sendButton_isDisabled = ref(false);
const userInput = ref("");  // 用户输入
const messages = ref([]);   // 消息列表
const isDialogOpen = ref(false);
const dynamicWidth = computed(() => (isDialogOpen.value ? '69%' : '100%')); // 根据 isDialogOpen 设置新闻块的宽度
const richTextEditor = ref(null); // 引用富文本编辑器元素
// 获取 ProseMirror 输入内容的函数
const handleInput = () => {
  const promptTextarea = document.getElementById('prompt-textarea');
  userInput.value = promptTextarea.innerText.trim(); // 获取编辑器中的文本内容
  console.log(userInput.value); // 打印输入内容，进行调试
};

// 模拟大模型的回复
const modelReply = (userMessage) => {
  return `大模型回复: 收到你的消息 - "${userMessage}"`;
};
// 发送消息
const sendMessage = () => {
  if (userInput.value.trim() === "") return;

  // 用户的消息
  messages.value.push({ type: 'user', content: userInput.value });

  // 模拟大模型的回复
  const reply = modelReply(userInput.value);
  setTimeout(() => {
    messages.value.push({ type: 'model', content: reply });
    scrollToBottom(); // 每次新消息加入后自动滚动到最底部
  }, 500);  // 模拟延迟回复

  // 清空输入框
  richTextEditor.value.innerHTML = '';
};
// 滚动到最底部
const scrollToBottom = () => {
  const box = messages.value;
  box.scrollTop = box.scrollHeight;
};
const toggleDialog = () => {
  isDialogOpen.value = !isDialogOpen.value;
};


// 聊天列表，初始带有一条 AI 消息
const chatList = ref([
  {
    id: 1,
    uid: '1002', // AI 助理的 uid
    name: 'AI助理',
    headImg: 'ai-avatar.png', // 替换为你使用的 AI 头像路径
    msg: '您好，有什么我可以帮忙的吗？',
    time: new Date().toLocaleTimeString(),
  },
]);

// 输入框内容
const inputMsg = ref('');

// 发送消息方法
const sendText = () => {
  if (inputMsg.value.trim() === '') return; // 如果输入为空，返回

  // 用户消息对象
  const userMessage = {
    id: chatList.value.length + 1,
    uid: '1001', // 用户的 uid
    name: '用户',
    headImg: 'user-avatar.png', // 替换为你使用的用户头像路径
    msg: inputMsg.value,
    time: new Date().toLocaleTimeString(),
  };

  // 将用户消息推送到聊天列表
  chatList.value.push(userMessage);

  // 清空输入框
  inputMsg.value = '';

  // 模拟 AI 回复
  setTimeout(() => {
    const aiMessage = {
      id: chatList.value.length + 1,
      uid: '1002', // AI 的 uid
      name: 'AI助理',
      headImg: 'ai-avatar.png', // 替换为 AI 头像
      msg: 'AI助理回复: ' + userMessage.msg,
      time: new Date().toLocaleTimeString(),
    };
    chatList.value.push(aiMessage);
  }, 1000); // 延迟 1 秒后 AI 回复
};

// 生成随机卡片类型
const randomCard = (index) => {
  return Math.random() > 0.5 ? 1 : 2; // 随机返回1或2
};

</script>

<template>
  <div id="app">
    <!-- 页眉 -->
    <header class="header">
      <!-- 页眉左半部分 -->
      <div class="logo-container">
        <img src="./components/logo.png" alt="Logo" class="logo" />
        <span class="logo-text">  News</span>
      </div>
      <!-- 页眉右半部分 -->
      <nav class="nav">
          <div class="head-icon" @click="Home">
            <img src="./components/主页.png">
          </div>

          <div class="head-icon" @click="Home">
            <img src="./components/收藏.png">
          </div>

          <div class="head-icon" @click="Home">
            <img src="./components/分类.png">
          </div>

          <div class="head-icon" @click="Home">
            <img src="./components/history.png">
          </div>

          <div class="head-icon" @click="Home">
            <img src="./components/查找.png">
          </div>

          <div class="head-icon" @click="Home">
            <img src="./components/个人.png">
          </div>
      </nav>

    </header>

    <!-- 主体 -->
    <main class="main">
      <!-- 新闻主体部分-->
      <div class="news-wrapper" :style="{ width: dynamicWidth }">
        <div class="news-container">
          <div v-for="(news, index) in newsList1" :key="news.id">
            <template v-if="randomCard(index) === 1">
              <div class="news-item" :style="{ backgroundImage: `url(${news.image})` }">
                <!--作者信息-->
                <div class = "pub-info-container flex ">
                  <!-- 头像 -->
                  <el-avatar size="small">User</el-avatar>
                  <!-- 作者名称 -->
                  <span class="author-name mr-4">Juju</span>
                  <!-- 年月日 -->
                  <span class="date">2024年10月8日</span>
                </div>
                <!--标题-->
                <h3 class="news-title">{{ news.title }}</h3>
                <!--标签 阅读 喜欢-->
                <div class="news-bottom">
                  <!--标签-->
                  <div class="rounded-box-table">
                    健康
                  </div>
                  <div style="display: flex; align-items: center; gap: 8px;margin-left: 100px;">
                    <!-- 爱心图标 -->
                    <img src="./components/赞.svg" alt="icon" width="16" height="16">
                    <!-- 点赞次数 -->
                    <span>123</span>
                    <!-- 眼睛图标 -->
                    <img src="./components/浏览.svg" alt="icon" width="16" height="16">
                    <!-- 浏览次数 -->
                    <span>456</span>
                  </div>
                </div>
              </div>  
            </template>
            <template v-else>
              <div class="news-item2">
                <!--新闻内容-->
                <div class="news-content">
                  <!--新闻配图-->
                  <img :src="news.image" style="height: 225px; width: 280px;">
                  
                  <!--作者信息-->
                  <div class="pub-info-container flex ">
                    <!-- 头像 -->
                    <el-avatar size="small">User</el-avatar>
                    <!-- 作者名称 -->
                    <span class="author-name-black mr-4">Juju</span>
                    <!-- 年月日 -->
                    <span class="date-black">2024年10月8日</span>
                  </div>
                  <!--标题-->
                  <h3 class="news-title-black">{{ news.title }}</h3>
                  <!--文章内容-->
                  <p style="font-size: 12px; color: #b0b0b0;text-align: left;   /* 左对齐 */ margin-left: 10px">{{ news.content }}</p>

                  <!--标签 阅读 喜欢-->
                  <div class="news-bottom">
                    <!--标签-->
                    <div class="rounded-box-table">
                      健康
                    </div>

                    <div style="display: flex; align-items: center; gap: 8px;margin-left: 100px;">
                      <!-- 爱心图标 -->
                      <img src="./components/赞.svg" alt="icon" width="16" height="16">
                      <!-- 点赞次数 -->
                      <span>123</span>
                      <!-- 眼睛图标 -->
                      <img src="./components/浏览.svg" alt="icon" width="16" height="16">
                      <!-- 浏览次数 -->
                      <span>456</span>
                    </div>
                  </div>
                </div>
              </div>
            </template>
          </div>
        </div>
        <div class="news-container">
          <div v-for="(news, index) in newsList2" :key="news.id">
            <template v-if="randomCard(index) === 1">
              <div class="news-item" :style="{ backgroundImage: `url(${news.image})` }">
                <!--作者信息-->
                <div class = "pub-info-container flex ">
                  <!-- 头像 -->
                  <el-avatar size="small">User</el-avatar>
                  <!-- 作者名称 -->
                  <span class="author-name mr-4">Juju</span>
                  <!-- 年月日 -->
                  <span class="date">2024年10月8日</span>
                </div>
                <!--标题-->
                <h3 class="news-title">{{ news.title }}</h3>
                <!--标签 阅读 喜欢-->
                <div class="news-bottom">
                  <!--标签-->
                  <div class="rounded-box-table">
                    健康
                  </div>
                  <div style="display: flex; align-items: center; gap: 8px;margin-left: 100px;">
                    <!-- 爱心图标 -->
                    <img src="./components/赞.svg" alt="icon" width="16" height="16">
                    <!-- 点赞次数 -->
                    <span>123</span>
                    <!-- 眼睛图标 -->
                    <img src="./components/浏览.svg" alt="icon" width="16" height="16">
                    <!-- 浏览次数 -->
                    <span>456</span>
                  </div>
                </div>
              </div>  
            </template>
            <template v-else>
              <div class="news-item2">
                <!--新闻内容-->
                <div class="news-content">
                  <!--新闻配图-->
                  <img :src="news.image" style="height: 225px; width: 280px;">
                  
                  <!--作者信息-->
                  <div class="pub-info-container flex ">
                    <!-- 头像 -->
                    <el-avatar size="small">User</el-avatar>
                    <!-- 作者名称 -->
                    <span class="author-name-black mr-4">Juju</span>
                    <!-- 年月日 -->
                    <span class="date-black">2024年10月8日</span>
                  </div>
                  <!--标题-->
                  <h3 class="news-title-black">{{ news.title }}</h3>
                  <!--文章内容-->
                  <p style="font-size: 12px; color: #b0b0b0;text-align: left;   /* 左对齐 */ margin-left: 10px">{{ news.content }}</p>

                  <!--标签 阅读 喜欢-->
                  <div class="news-bottom">
                    <!--标签-->
                    <div class="rounded-box-table">
                      健康
                    </div>

                    <div style="display: flex; align-items: center; gap: 8px;margin-left: 100px;">
                      <!-- 爱心图标 -->
                      <img src="./components/赞.svg" alt="icon" width="16" height="16">
                      <!-- 点赞次数 -->
                      <span>123</span>
                      <!-- 眼睛图标 -->
                      <img src="./components/浏览.svg" alt="icon" width="16" height="16">
                      <!-- 浏览次数 -->
                      <span>456</span>
                    </div>
                  </div>
                </div>
              </div>
            </template>
          </div>
        </div>
        <div class="news-container">
          <div v-for="(news, index) in newsList3" :key="news.id">
            <template v-if="randomCard(index) === 1">
              <div class="news-item" :style="{ backgroundImage: `url(${news.image})` }">
                <!--作者信息-->
                <div class = "pub-info-container flex ">
                  <!-- 头像 -->
                  <el-avatar size="small">User</el-avatar>
                  <!-- 作者名称 -->
                  <span class="author-name mr-4">Juju</span>
                  <!-- 年月日 -->
                  <span class="date">2024年10月8日</span>
                </div>
                <!--标题-->
                <h3 class="news-title">{{ news.title }}</h3>
                <!--标签 阅读 喜欢-->
                <div class="news-bottom">
                  <!--标签-->
                  <div class="rounded-box-table">
                    健康
                  </div>
                  <div style="display: flex; align-items: center; gap: 8px;margin-left: 100px;">
                    <!-- 爱心图标 -->
                    <img src="./components/赞.svg" alt="icon" width="16" height="16">
                    <!-- 点赞次数 -->
                    <span>123</span>
                    <!-- 眼睛图标 -->
                    <img src="./components/浏览.svg" alt="icon" width="16" height="16">
                    <!-- 浏览次数 -->
                    <span>456</span>
                  </div>
                </div>
              </div>  
            </template>
            <template v-else>
              <div class="news-item2">
                <!--新闻内容-->
                <div class="news-content">
                  <!--新闻配图-->
                  <img :src="news.image" style="height: 225px; width: 280px;">
                  
                  <!--作者信息-->
                  <div class="pub-info-container flex ">
                    <!-- 头像 -->
                    <el-avatar size="small">User</el-avatar>
                    <!-- 作者名称 -->
                    <span class="author-name-black mr-4">Juju</span>
                    <!-- 年月日 -->
                    <span class="date-black">2024年10月8日</span>
                  </div>
                  <!--标题-->
                  <h3 class="news-title-black">{{ news.title }}</h3>
                  <!--文章内容-->
                  <p style="font-size: 12px; color: #b0b0b0;text-align: left;   /* 左对齐 */ margin-left: 10px">{{ news.content }}</p>

                  <!--标签 阅读 喜欢-->
                  <div class="news-bottom">
                    <!--标签-->
                    <div class="rounded-box-table">
                      健康
                    </div>

                    <div style="display: flex; align-items: center; gap: 8px;margin-left: 100px;">
                      <!-- 爱心图标 -->
                      <img src="./components/赞.svg" alt="icon" width="16" height="16">
                      <!-- 点赞次数 -->
                      <span>123</span>
                      <!-- 眼睛图标 -->
                      <img src="./components/浏览.svg" alt="icon" width="16" height="16">
                      <!-- 浏览次数 -->
                      <span>456</span>
                    </div>
                  </div>
                </div>
              </div>
            </template>
          </div>
        </div>
        <div class="news-container">
          <div v-for="(news, index) in newsList4" :key="news.id">
            <template v-if="randomCard(index) === 1">
              <div class="news-item" :style="{ backgroundImage: `url(${news.image})` }">
                <!--作者信息-->
                <div class = "pub-info-container flex ">
                  <!-- 头像 -->
                  <el-avatar size="small">User</el-avatar>
                  <!-- 作者名称 -->
                  <span class="author-name mr-4">Juju</span>
                  <!-- 年月日 -->
                  <span class="date">2024年10月8日</span>
                </div>
                <!--标题-->
                <h3 class="news-title">{{ news.title }}</h3>
                <!--标签 阅读 喜欢-->
                <div class="news-bottom">
                  <!--标签-->
                  <div class="rounded-box-table">
                    健康
                  </div>
                  <div style="display: flex; align-items: center; gap: 8px;margin-left: 100px;">
                    <!-- 爱心图标 -->
                    <img src="./components/赞.svg" alt="icon" width="16" height="16">
                    <!-- 点赞次数 -->
                    <span>123</span>
                    <!-- 眼睛图标 -->
                    <img src="./components/浏览.svg" alt="icon" width="16" height="16">
                    <!-- 浏览次数 -->
                    <span>456</span>
                  </div>
                </div>
              </div>  
            </template>
            <template v-else>
              <div class="news-item2">
                <!--新闻内容-->
                <div class="news-content">
                  <!--新闻配图-->
                  <img :src="news.image" style="height: 225px; width: 280px;">
                  
                  <!--作者信息-->
                  <div class="pub-info-container flex ">
                    <!-- 头像 -->
                    <el-avatar size="small">User</el-avatar>
                    <!-- 作者名称 -->
                    <span class="author-name-black mr-4">Juju</span>
                    <!-- 年月日 -->
                    <span class="date-black">2024年10月8日</span>
                  </div>
                  <!--标题-->
                  <h3 class="news-title-black">{{ news.title }}</h3>
                  <!--文章内容-->
                  <p style="font-size: 12px; color: #b0b0b0;text-align: left;   /* 左对齐 */ margin-left: 10px">{{ news.content }}</p>

                  <!--标签 阅读 喜欢-->
                  <div class="news-bottom">
                    <!--标签-->
                    <div class="rounded-box-table">
                      健康
                    </div>

                    <div style="display: flex; align-items: center; gap: 8px;margin-left: 100px;">
                      <!-- 爱心图标 -->
                      <img src="./components/赞.svg" alt="icon" width="16" height="16">
                      <!-- 点赞次数 -->
                      <span>123</span>
                      <!-- 眼睛图标 -->
                      <img src="./components/浏览.svg" alt="icon" width="16" height="16">
                      <!-- 浏览次数 -->
                      <span>456</span>
                    </div>
                  </div>
                </div>
              </div>
            </template>
          </div>
        </div>
      </div>
      
      <!-- 悬浮按钮以及对话框 -->
      <div v-if="!isDialogOpen">
        <!-- 悬浮按钮 -->
        <button class="floating-button" @click="toggleDialog">
          <img id="rotating-ai-assistant" src="../public/ai-assistant.png" alt="floating button icon" class="button-icon" style="margin-left: 10px;">
        </button>
      </div>
      <div>
        <!-- 对话框 -->
        <transition 
          enter-active-class="animate__animated animate__slideInRight"
          leave-active-class="animate__animated animate__slideOutRight"
        >
          <div v-if="isDialogOpen" class="dialog">
            <!-- 对话框页眉 --> 
            <div class="dialog-header">
              <!-- 左上角的 Logo 和 AI 助理文字 -->
              <img src="../public/ai-assistant.png" alt="Logo" class="dialog-logo">
              <span class="dialog-title">AI助理</span>
              <!-- 关闭按钮 -->
              <button class="close-button" @click="toggleDialog">&times;</button>
            </div>

            <!-- 提示块 -->
            <div class="dialog-tips">
              <div style="background-image: url('../public/hello.png'); background-repeat: no-repeat;text-align: left; font-family: Arial, sans-serif; font-size: 20px;">
                <div style="margin-left: 5px;">
                  <p style="">您好</p>
                  <p>我是您的专属AI</p>
                </div>
              </div>
             
               <!-- 添加横线 -->
              <hr class="dialog-tips-divider" />
              <p style="font-family: Arial, sans-serif; text-align: left;font-size: 16px;font-weight: 500;">点击左侧卡片，我可以为您总结新闻~</p>
              <!-- Tips列表 -->
              <ul class="dialog-tips-list">
                <li>来点今日的热点新闻听听如何？</li>
                <li>推荐最新的体育新闻</li>
              </ul>
            </div>

            <!-- 聊天交流框 -->
            <div class="chat-box">
              <div class="messages">
                <div v-for="(message, index) in messages" :key="index" :class="['message', message.type]">
                  <!-- 用户头像和用户名 -->
                  <div class="avatar-container" :class="{ 'reverse': message.type === 'model' }">
                    <div class="username">{{ message.type === 'user' ? '用户' : 'AI助理' }}</div>
                    <img v-if="message.type === 'user'" class="avatar" src="../public/user.png" alt="用户头像" >
                    <img v-if="message.type === 'model'" class="avatar" src="../public/ai-assistant.png" alt="AI头像">
                  </div>
                  <div class="message-content">
                    <div class="bubble">{{ message.content }}</div>
                  </div>
                </div>
              </div>
            </div>
            <!-- 输入框-->
            <div class="flex w-full flex-col gap-1.5 rounded-[26px] p-1.5 transition-colors
             bg-[#f4f4f4] dark:bg-token-main-surface-secondary flex-grow-1 " 
             style="position: absolute;bottom: 20px;right: 55px;max-width: 350px;">
              <div class="flex items-center gap-1.5 pl-4 md:gap-2">
                <!-- 消息输入框部分 -->
                <div class="flex min-w-0 flex-1 flex-col">
                  <div class="_prosemirror-parent_15ceg_1  max-h-[15dvh] max-h-52 overflow-auto default-browser">
                    <!-- ProseMirror 富文本编辑器 -->
                    <div contenteditable="true" translate="no" class="ProseMirror" id="prompt-textarea"
                    @input="handleInput" ref="richTextEditor">
                      <p data-placeholder="发送消息" class="placeholder">
                        <br class="ProseMirror-trailingBreak">
                      </p>
                    </div>
                  </div>
                </div>

                <!-- 发送按钮部分 -->
                <div class="min-w-8">
                  <button 
                    :disabled="sendButton_isDisabled" 
                    aria-label="发送提示" 
                    data-testid="send-button"
                    @click="sendMessage"  
                    class="mb-1 me-1 flex h-8 w-8 items-center justify-center rounded-full bg-black text-white transition-colors hover:opacity-70 focus-visible:outline-none focus-visible:outline-black disabled:text-[#f4f4f4] disabled:hover:opacity-100 dark:bg-white dark:text-black dark:focus-visible:outline-white disabled:dark:bg-token-text-quaternary dark:disabled:text-token-main-surface-secondary disabled:bg-[#D7D7D7]">
                      <svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg" class="icon-2xl">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M15.1918 8.90615C15.6381 8.45983 16.3618 8.45983 16.8081 8.90615L21.9509 14.049C22.3972 14.4953 22.3972 15.2189 21.9509 15.6652C21.5046 16.1116 20.781 16.1116 20.3347 15.6652L17.1428 12.4734V22.2857C17.1428 22.9169 16.6311 23.4286 15.9999 23.4286C15.3688 23.4286 14.8571 22.9169 14.8571 22.2857V12.4734L11.6652 15.6652C11.2189 16.1116 10.4953 16.1116 10.049 15.6652C9.60265 15.2189 9.60265 14.4953 10.049 14.049L15.1918 8.90615Z" fill="currentColor"></path>
                      </svg>
                  </button>
                </div>
              </div>
            </div>

            
            
          </div>
        </transition>
      </div>

    </main>
  </div>
</template>

<style scoped>
.news-bottom{
  position: absolute;             /* 设置子级元素为绝对定位 */
  bottom: 10px;                     /* 将子级元素固定在底部 */
  margin-left: 10px;
  display: flex;
}
.rounded-box-table {
  display: flex;                  /* 使用 flexbox 对齐内容 */
  justify-content: center;        /* 水平居中 */
  align-items: center;            /* 垂直居中 */
  width: 40px;                   /* 设置宽度 */
  height: 20px;                   /* 设置高度 */
  background-color: transparent;  /* 设置背景色为透明 */
  border: 2px solid #D3D3D3;     /* 设置边框为浅灰色 */
  color: #D3D3D3;                 /* 设置字体颜色与边框相同 */
  border-radius: 15px;            /* 设置圆角半径 */
  font-size: 10px;                /* 设置字体大小 */
  font-weight: bold;              /* 设置字体加粗 */
}
/* 自定义作者名称的样式 */
.author-name {
  font-size: 16px; /* 设置字体大小 */

  color: #ffffffcf; /* 设置字体颜色 */
}
.author-name-black {
  font-size: 16px; /* 设置字体大小 */

  color: #060606e4; /* 设置字体颜色 */
}
.date{
  font-size: 16px; /* 设置字体大小 */

  color: #ffffffcf; /* 设置字体颜色 */
}
.date-black{
  font-size: 16px; /* 设置字体大小 */

  color: #060606e4; /* 设置字体颜色 */
}
.pub-info-container{
  margin-left: 10px;
  margin-top: 10px;
  gap: 5px;
}
.ProseMirror:focus {
  outline: none; /* 移除默认的黑色边框 */
}
.custom-input {
  width: 100%; /* 根据需要调整宽度 */
  height: 40px; /* 设置固定高度 */
  padding: 10px; /* 内边距 */
  font-size: 16px; /* 字体大小 */
  border: 2px solid lightblue; /* 浅蓝色边框 */
  border-radius: 20px; /* 将两端设置为圆形 */
  outline: none; /* 去除点击时的默认轮廓 */
  box-sizing: border-box; /* 确保padding不会影响输入框整体大小 */
}

.custom-input::placeholder {
  color: #999; /* 提示文字颜色 */
  font-style: italic; /* 提示文字样式（可选） */
}
/* 聊天框样式 */
.chat-box {
  height: 260px; /* 定义固定高度，可以根据需要调整 */
  flex-grow: 1; /* 动态填充剩余空间 */
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.messages {
  flex: 1;
  overflow-y: auto;
  padding: 10px;

  margin-bottom: 10px;

  border-radius: 8px;
}

.message {
  display: flex;
  flex-direction: column;
  margin-bottom: 10px;
}

.message.user {
  align-items: flex-end; /* 用户消息靠右 */
}

.message.model {
  align-items: flex-start; /* 模型消息靠左 */
}

/* 用户头像和用户名在一行 */
.avatar-container {
  display: flex;
  align-items: center; /* 垂直居中 */
  margin-bottom: 5px; /* 控制头像与气泡的间距 */
}

/* AI助理消息：用户名在头像右侧，反转顺序 */
.avatar-container.reverse {
  flex-direction: row-reverse; /* 头像在右，用户名在左 */
}

.avatar {
  width: 40px; /* 调整用户头像大小 */
  height: 40px;
  border-radius: 50%;
  margin-right: 10px;
  
}

.avatar-container.reverse .avatar {
  margin-right: 0; /* 去掉反转时的右边距 */
  margin-left: 10px; /* 给头像加左边距 */
}

.username {
  font-size: 14px;
  color: #000000;
}

.message-content {
  max-width: 60%;
}

.bubble {
  background-color: #e5e5ea; /* 模型消息气泡颜色 */
  border-radius: 15px;
  padding: 6px 10px; /* 减少上下的 padding */
  font-size: 14px;
  display: inline-block;
  margin-right: 15px;
  font-size: 14px;
}

.message.user .bubble {
  background-color: #ADD8E6; /* 用户消息气泡颜色 */
  color: white;
}

/* 输入框样式 */
.message-input {
  display: flex;
  gap: 13px;
  flex-grow: 1; /* 动态填充剩余空间 */
}

.message-input input {
  flex: 1;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.message-input button {
  padding: 10px 20px;
  border: none;
  background-color: #007bff;
  color: white;
  cursor: pointer;
  border-radius: 4px;
}

.message-input button:hover {
  background-color: #0056b3;
}

/* 提示块部分样式 */
.dialog-tips {
  border: 1px solid #ccc; /* 提示块的边框 */
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
  background-color: #fff;
   /* 添加阴影效果，上方无阴影，左右轻微，下方重 */
   box-shadow: 
    0 0px 0px rgba(0, 0, 0, 0), /* 上边框无阴影 */
    4px 0 8px rgba(0, 0, 0, 0.05), /* 左边框阴影 */
    -4px 0 8px rgba(0, 0, 0, 0.05), /* 右边框阴影 */
    0 8px 16px rgba(0, 0, 0, 0.2); /* 下边框阴影最重 */
    width: 370px;
}

.dialog-tips-divider {
  border: none;
  border-top: 1px solid #ddd;
  margin: 10px 0;
}

.dialog-tips-list {
  list-style: none;
  padding: 0;
  font-size: 14px;
}

.dialog-tips-list li {
  text-align: left;
  background-color: #f0f0f0;
  border-radius: 8px;
  padding: 6px 8px; /* 减少内边距 */
  margin: 3px 0;    /* 减少上下间距 */
  line-height: 1.3; /* 减少行高，使文本更紧凑 */
  margin: 10px 0;
}
.close-button {
  background: none;
  border: none;
  font-size: 1.5em; /* 设置关闭按钮的大小 */
  cursor: pointer;
  color: #333; /* 设置关闭按钮的颜色 */
  padding: 0; /* 去掉按钮的默认内边距 */
  margin-left: auto; /* 将关闭按钮与文字拉开距离 */
}
.dialog-logo {
  width: 40px; /* Logo 大小 */
  height: 40px;
  margin-right: 10px; /* 调整 Logo 和文字之间的间距 */
}
.dialog-header {
  display: flex;
  align-items: center;
  justify-content: space-between; /* 使关闭按钮在右侧 */
  margin-bottom: 20px; /* 调整与下方内容的距离 */
}
/*
悬浮窗css样式
*/
.floating-button {
  position: fixed;
  top: 120px;
  right: 0;                   /* 让按钮贴着屏幕右边缘 */
  
  background-color: white;     /* 设置背景色为白色 */
  color: black;                /* 设置文本颜色为黑色 */

  border-radius: 25px 0 0 25px; /* 左上角和左下角圆角，右侧直角 */
  
  width: 100px;
  height: 100px;
  font-size: 24px;
  cursor: pointer;
  
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1); /* 轻微阴影效果 */
}

.dialog {
  position: relative;
  width: 440px;
  margin-right: 20px;
  height: calc(100vh - 100px);
  background-color: white;
  border: none; /* 去除边框 */
  border-radius: 15px; /* 圆角 */
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.15); /* 添加更明显的阴影 */
  position: fixed;
  right: 0;
  top: 70px;
  transform: translateY(-0%);
  padding: 20px;
  z-index: 1000;
}

.dialog-enter-active, .dialog-leave-active {
  transition: transform 0.3s ease;
}

.dialog-enter, .dialog-leave-to {
  transform: translateX(100%);
}

.dialog-enter-to, .dialog-leave {
  transform: translateX(0);
}


#app {
  font-family:Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
}

.header {
  display: flex; /* 使用flex布局 */
  justify-content: space-between; /* 在两侧对齐 */
  align-items: center; /* 垂直居中对齐 */
  padding: 10px 20px;
  background-color: #ffffff;
  color: white;
  height: 60px
}

.nav{
  display: flex; /* 使用flex布局 */
}


.head-icon{
  display: flex; /* 使用flex布局 */
  justify-content: space-between; /* 在两侧对齐 */
  align-items: center; /* 垂直居中对齐 */
  cursor: pointer; /* 鼠标悬停时显示手指光标 */
  width: 40px; /* 图标容器宽度 */
  height: 40px; /* 图标容器高度 */
  transition: fill 0.3s; /* 颜色过渡效果 */
}

.head-icon img {
  width: 24px; /* 图标宽度 */
  height: 24px; /* 图标高度 */
  transition: opacity 0.3s; /* 透明度过渡效果 */
}

.head-icon:hover img {
  opacity: 0.7; /* 鼠标悬停时改变透明度 */
}

.logo-text {
  font-size: 1.5em; /* 设置文本大小 */
  font-weight: bold; /* 设置文本加粗 */
  color: rgb(110, 24, 248);
}

.logo-container {
  display: flex; /* 使用flex布局 */
  align-items: center; /* 垂直居中对齐 */
}



.main {
  
  height: calc(100vh - 60px); /* 假设头部高度为60px，替换为实际高度 */
  overflow: hidden; /* 防止溢出 */
  padding: 20px;
}

.news-wrapper {
  display: flex;                /* 使用 Flexbox 布局 */
  gap: 40px;
  height: 100%; /* 垂直方向占满 */
  overflow-y: auto; /* 启用垂直滚动条 */
  padding: 10px;
  box-sizing: border-box; /* 包含内边距在宽高内 */
}

.news-container {
  display: flex;                /* 启用Flexbox布局 */
  flex-direction: column;       /* 设置为竖直方向排列 */
  align-items: flex-start;      /* 卡片左对齐 */
  gap: 20px;                    /* 卡片之间的间距 */
  padding: 5px;
}

.news-item {
  position: relative;
  background-color: #f8f8f8; /* 矩形背景颜色 */

  border: 1px solid #ccc; /* 边框 */
  border-radius: 8px; /* 圆角 */
  overflow: hidden; /* 防止内容溢出 */
  transition: transform 0.3s; /* 动效 */
  box-shadow: var(--el-box-shadow-lighter);
  background-size: cover;
  width: 300px; height: 225px;
}
.news-item2{
  border: 1px solid #ccc; /* 边框 */
  border-radius: 8px; /* 圆角 */
  overflow: hidden; /* 防止内容溢出 */
  transition: transform 0.3s; /* 动效 */
  box-shadow: var(--el-box-shadow-lighter);
  width: 300px; height: 450px;
  display: flex;                /* 启用flexbox布局 */
  justify-content: center;      /* 水平居中 */
  align-items: center;          /* 垂直居中 */
}
.news-content{
  position: relative;
  border-radius: 8px; /* 圆角 */
  overflow: hidden; /* 防止内容溢出 */
  transition: transform 0.3s; /* 动效 */

  width: 280px; height: 430px;
}
.news-item2:hover{
  transform: scale(1.05); /* 鼠标悬停时放大 */
}
.news-item:hover {
  transform: scale(1.05); /* 鼠标悬停时放大 */
}

.news-image {
  width: 100%; /* 图片占满整个矩形 */
  height: auto; /* 自适应高度 */
  aspect-ratio: 1; /* 保持方形 */
}

.news-title {
  padding: 10px; /* 标题内边距 */
  font-size: 1.2em; /* 标题字体大小 */
  text-align: center; /* 标题居中 */
  color: #ffffff; /* 标题颜色 */
  margin-top: 80px;
  text-align: left; /* 设置标题左对齐 */
}
.news-title-black {
  padding: 10px; /* 标题内边距 */
  font-size: 1.2em; /* 标题字体大小 */
  text-align: center; /* 标题居中 */
  color: #060606e4; /* 标题颜色 */
  margin-top: 8px;
  text-align: left; /* 设置标题左对齐 */
}




</style>


