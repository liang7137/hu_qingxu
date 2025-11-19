<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>学生情绪记录工具</title>
  <!-- 引入外部资源 -->
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.8/dist/chart.umd.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/xlsx@0.18.5/dist/xlsx.full.min.js"></script>
  
  <!-- 配置Tailwind -->
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            primary: '#4F46E5',
            secondary: '#10B981',
            warning: '#F59E0B',
            danger: '#EF4444',
          },
          fontFamily: {
            sans: ['Inter', 'system-ui', 'sans-serif'],
          },
        },
      }
    }
  </script>
  
  <style type="text/tailwindcss">
    @layer utilities {
      .content-auto {
        content-visibility: auto;
      }
      .card-shadow {
        box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
      }
      .transition-custom {
        transition: all 0.3s ease;
      }
    }
  </style>
</head>
<body class="bg-gray-50 font-sans text-gray-800 min-h-screen">
  <!-- 导航栏 -->
  <nav class="bg-white shadow-md fixed w-full top-0 z-50 transition-custom">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16">
        <div class="flex items-center">
          <a href="#" class="flex items-center space-x-2">
            <i class="fa fa-heart-o text-primary text-2xl"></i>
            <span class="font-bold text-xl text-primary">情绪记录助手</span>
          </a>
        </div>
        <div class="flex items-center space-x-4">
          <button id="studentLoginBtn" class="px-4 py-2 rounded-md text-sm font-medium text-primary hover:text-primary/80 transition-custom">
            学生登录
          </button>
          <button id="counselorLoginBtn" class="px-4 py-2 bg-primary text-white rounded-md text-sm font-medium hover:bg-primary/90 transition-custom">
            辅导员登录
          </button>
        </div>
      </div>
    </div>
  </nav>

  <!-- 主内容区 -->
  <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 pt-24 pb-16">
    <!-- 登录选择页面 -->
    <div id="loginSelection" class="py-12">
      <div class="text-center mb-12">
        <h1 class="text-[clamp(1.8rem,4vw,2.5rem)] font-bold text-gray-900 mb-4">每日情绪记录</h1>
        <p class="text-lg text-gray-600 max-w-2xl mx-auto">
          记录你的每日情绪状态，帮助我们更好地了解和支持你
        </p>
      </div>
      
      <div class="grid md:grid-cols-2 gap-8 max-w-4xl mx-auto">
        <!-- 学生入口卡片 -->
        <div class="bg-white rounded-xl p-8 card-shadow hover:shadow-lg transition-custom cursor-pointer transform hover:-translate-y-1" id="studentCard">
          <div class="w-16 h-16 bg-primary/10 rounded-full flex items-center justify-center mb-6 mx-auto">
            <i class="fa fa-user-o text-primary text-2xl"></i>
          </div>
          <h3 class="text-xl font-semibold text-center mb-3">学生端</h3>
          <p class="text-gray-600 text-center mb-6">使用学号和密码登录，记录每日情绪</p>
          <button class="w-full py-3 bg-white border border-primary text-primary rounded-lg font-medium hover:bg-primary/5 transition-custom">
            进入学生端
          </button>
        </div>
        
        <!-- 辅导员入口卡片 -->
        <div class="bg-white rounded-xl p-8 card-shadow hover:shadow-lg transition-custom cursor-pointer transform hover:-translate-y-1" id="counselorCard">
          <div class="w-16 h-16 bg-primary/10 rounded-full flex items-center justify-center mb-6 mx-auto">
            <i class="fa fa-bar-chart text-primary text-2xl"></i>
          </div>
          <h3 class="text-xl font-semibold text-center mb-3">辅导员端</h3>
          <p class="text-gray-600 text-center mb-6">查看学生情绪统计，管理学生账号</p>
          <button class="w-full py-3 bg-primary text-white rounded-lg font-medium hover:bg-primary/90 transition-custom">
            进入辅导员端
          </button>
        </div>
      </div>
    </div>

    <!-- 学生登录表单 -->
    <div id="studentLogin" class="py-12 hidden">
      <div class="max-w-md mx-auto bg-white rounded-xl p-8 card-shadow">
        <h2 class="text-2xl font-bold text-center mb-6">学生登录</h2>
        <form id="studentLoginForm">
          <div class="mb-4">
            <label for="studentId" class="block text-sm font-medium text-gray-700 mb-1">学号</label>
            <input type="text" id="studentId" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请输入学号" required>
          </div>
          <div class="mb-6">
            <label for="studentPassword" class="block text-sm font-medium text-gray-700 mb-1">密码</label>
            <input type="password" id="studentPassword" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请输入密码" required>
          </div>
          <button type="submit" class="w-full py-3 bg-primary text-white rounded-lg font-medium hover:bg-primary/90 transition-custom">
            登录
          </button>
        </form>
        <button id="backFromStudentLogin" class="mt-4 w-full py-2 text-gray-600 hover:text-gray-900 transition-custom">
          <i class="fa fa-arrow-left mr-1"></i> 返回
        </button>
      </div>
    </div>

    <!-- 学生情绪记录页面 -->
    <div id="studentEmotionForm" class="py-12 hidden">
      <div class="max-w-md mx-auto bg-white rounded-xl p-8 card-shadow">
        <div class="flex justify-between items-center mb-6">
          <h2 class="text-2xl font-bold">记录今日情绪</h2>
          <span id="currentDate" class="text-gray-500"></span>
        </div>
        
        <div id="studentInfo" class="mb-8 p-4 bg-gray-50 rounded-lg flex justify-between items-center">
          <div>
            <p><span class="font-medium">学号：</span><span id="displayStudentId"></span></p>
            <p><span class="font-medium">姓名：</span><span id="displayStudentName"></span></p>
          </div>
          <button id="studentChangePwdBtn" class="text-primary text-sm hover:underline transition-custom">
            修改密码
          </button>
        </div>
        
        <form id="emotionForm">
          <div class="space-y-4 mb-8">
            <label class="flex items-center p-4 border border-gray-200 rounded-lg cursor-pointer hover:bg-gray-50 transition-custom">
              <input type="radio" name="emotion" value="开心" class="w-5 h-5 text-secondary focus:ring-secondary" required>
              <div class="ml-4">
                <span class="block text-lg font-medium">开心</span>
                <span class="text-gray-500 text-sm">今天感觉很愉快，一切顺利</span>
              </div>
              <i class="fa fa-smile-o ml-auto text-2xl text-secondary"></i>
            </label>
            
            <label class="flex items-center p-4 border border-gray-200 rounded-lg cursor-pointer hover:bg-gray-50 transition-custom">
              <input type="radio" name="emotion" value="平淡" class="w-5 h-5 text-warning focus:ring-warning">
              <div class="ml-4">
                <span class="block text-lg font-medium">平淡</span>
                <span class="text-gray-500 text-sm">今天没什么特别的，和平常一样</span>
              </div>
              <i class="fa fa-meh-o ml-auto text-2xl text-warning"></i>
            </label>
            
            <label class="flex items-center p-4 border border-gray-200 rounded-lg cursor-pointer hover:bg-gray-50 transition-custom">
              <input type="radio" name="emotion" value="有点焦虑" class="w-5 h-5 text-danger focus:ring-danger">
              <div class="ml-4">
                <span class="block text-lg font-medium">有点焦虑</span>
                <span class="text-gray-500 text-sm">今天有些担心，感觉有压力</span>
              </div>
              <i class="fa fa-frown-o ml-auto text-2xl text-danger"></i>
            </label>
          </div>
          
          <div class="mb-4">
            <label for="notes" class="block text-sm font-medium text-gray-700 mb-1">备注（可选）</label>
            <textarea id="notes" rows="3" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="有什么想补充的可以写在这里..."></textarea>
          </div>
          
          <button type="submit" class="w-full py-3 bg-primary text-white rounded-lg font-medium hover:bg-primary/90 transition-custom">
            提交记录
          </button>
        </form>
        
        <button id="studentLogout" class="mt-4 w-full py-2 text-gray-600 hover:text-gray-900 transition-custom">
          退出登录
        </button>
      </div>
    </div>

    <!-- 学生修改密码表单 -->
    <div id="studentChangePassword" class="py-12 hidden">
      <div class="max-w-md mx-auto bg-white rounded-xl p-8 card-shadow">
        <h2 class="text-2xl font-bold text-center mb-6">修改密码</h2>
        <form id="studentChangePwdForm">
          <div class="mb-4">
            <label for="oldStudentPwd" class="block text-sm font-medium text-gray-700 mb-1">原密码</label>
            <input type="password" id="oldStudentPwd" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请输入原密码" required>
          </div>
          <div class="mb-4">
            <label for="newStudentPwd" class="block text-sm font-medium text-gray-700 mb-1">新密码</label>
            <input type="password" id="newStudentPwd" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请输入新密码" required>
            <p class="text-xs text-gray-500 mt-1">密码长度至少6位</p>
          </div>
          <div class="mb-6">
            <label for="confirmStudentPwd" class="block text-sm font-medium text-gray-700 mb-1">确认新密码</label>
            <input type="password" id="confirmStudentPwd" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请再次输入新密码" required>
          </div>
          <button type="submit" class="w-full py-3 bg-primary text-white rounded-lg font-medium hover:bg-primary/90 transition-custom">
            确认修改
          </button>
        </form>
        <button id="backToEmotionForm" class="mt-4 w-full py-2 text-gray-600 hover:text-gray-900 transition-custom">
          <i class="fa fa-arrow-left mr-1"></i> 返回
        </button>
      </div>
    </div>

    <!-- 辅导员登录表单 -->
    <div id="counselorLogin" class="py-12 hidden">
      <div class="max-w-md mx-auto bg-white rounded-xl p-8 card-shadow">
        <h2 class="text-2xl font-bold text-center mb-6">辅导员登录</h2>
        <form id="counselorLoginForm">
          <div class="mb-4">
            <label for="counselorUsername" class="block text-sm font-medium text-gray-700 mb-1">用户名</label>
            <input type="text" id="counselorUsername" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请输入用户名" required>
          </div>
          <div class="mb-6">
            <label for="counselorPassword" class="block text-sm font-medium text-gray-700 mb-1">密码</label>
            <input type="password" id="counselorPassword" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请输入密码" required>
          </div>
          <button type="submit" class="w-full py-3 bg-primary text-white rounded-lg font-medium hover:bg-primary/90 transition-custom">
            登录
          </button>
        </form>
        <button id="backFromCounselorLogin" class="mt-4 w-full py-2 text-gray-600 hover:text-gray-900 transition-custom">
          <i class="fa fa-arrow-left mr-1"></i> 返回
        </button>
      </div>
    </div>

    <!-- 辅导员修改密码表单 -->
    <div id="counselorChangePassword" class="py-12 hidden">
      <div class="max-w-md mx-auto bg-white rounded-xl p-8 card-shadow">
        <h2 class="text-2xl font-bold text-center mb-6">修改登录密码</h2>
        <form id="counselorChangePwdForm">
          <div class="mb-4">
            <label for="oldCounselorPwd" class="block text-sm font-medium text-gray-700 mb-1">原密码</label>
            <input type="password" id="oldCounselorPwd" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请输入原密码" required>
          </div>
          <div class="mb-4">
            <label for="newCounselorPwd" class="block text-sm font-medium text-gray-700 mb-1">新密码</label>
            <input type="password" id="newCounselorPwd" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请输入新密码" required>
            <p class="text-xs text-gray-500 mt-1">密码长度至少6位</p>
          </div>
          <div class="mb-6">
            <label for="confirmCounselorPwd" class="block text-sm font-medium text-gray-700 mb-1">确认新密码</label>
            <input type="password" id="confirmCounselorPwd" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请再次输入新密码" required>
          </div>
          <button type="submit" class="w-full py-3 bg-primary text-white rounded-lg font-medium hover:bg-primary/90 transition-custom">
            确认修改
          </button>
        </form>
        <button id="backToDashboard" class="mt-4 w-full py-2 text-gray-600 hover:text-gray-900 transition-custom">
          <i class="fa fa-arrow-left mr-1"></i> 返回
        </button>
      </div>
    </div>

    <!-- 辅导员数据查看页面 -->
    <div id="counselorDashboard" class="py-12 hidden">
      <div class="flex justify-between items-center mb-8">
        <h2 class="text-2xl font-bold">学生情绪统计</h2>
        <div class="flex items-center space-x-4">
          <button id="counselorChangePwdBtn" class="px-4 py-2 border border-primary text-primary rounded-md text-sm font-medium hover:bg-primary/5 transition-custom">
            修改密码
          </button>
          <button id="counselorLogout" class="px-4 py-2 text-gray-600 hover:text-gray-900 transition-custom">
            退出登录
          </button>
        </div>
      </div>
      
      <!-- 学生账号导入区域 -->
      <div class="bg-white rounded-xl p-6 card-shadow mb-8">
        <h3 class="text-lg font-semibold mb-4">学生账号管理</h3>
        <div class="flex flex-col sm:flex-row items-start sm:items-center gap-4">
          <div class="flex-1">
            <label class="block text-sm font-medium text-gray-700 mb-1">导入学生账号（Excel/CSV）</label>
            <input type="file" id="studentFile" accept=".xlsx,.xls,.csv" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:ring-2 focus:ring-primary focus:border-primary">
            <p class="text-xs text-gray-500 mt-1">文件格式：第一列"学号"，第二列"姓名"，第三列"密码"</p>
          </div>
          <div class="flex gap-3">
            <button id="importStudents" class="px-4 py-2 bg-primary text-white rounded-lg font-medium hover:bg-primary/90 transition-custom">
              导入账号
            </button>
            <button id="exportStudents" class="px-4 py-2 bg-white border border-primary text-primary rounded-lg font-medium hover:bg-primary/5 transition-custom">
              导出账号
            </button>
            <button id="checkStudents" class="px-4 py-2 bg-white border border-warning text-warning rounded-lg font-medium hover:bg-warning/5 transition-custom">
              查看账号
            </button>
          </div>
        </div>
        <div class="mt-4 text-sm text-gray-600">
          <span id="studentCount">当前学生账号数量：0人</span>
        </div>
      </div>
      
      <!-- 统计概览 -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
        <div class="bg-white rounded-xl p-6 card-shadow">
          <div class="flex items-center justify-between">
            <div>
              <p class="text-gray-500 text-sm">今日记录人数</p>
              <h3 class="text-3xl font-bold mt-1" id="totalStudents">0</h3>
            </div>
            <div class="w-12 h-12 bg-primary/10 rounded-full flex items-center justify-center">
              <i class="fa fa-users text-primary text-xl"></i>
            </div>
          </div>
        </div>
        
        <div class="bg-white rounded-xl p-6 card-shadow">
          <div class="flex items-center justify-between">
            <div>
              <p class="text-gray-500 text-sm">开心比例</p>
              <h3 class="text-3xl font-bold mt-1 text-secondary" id="happyPercentage">0%</h3>
            </div>
            <div class="w-12 h-12 bg-secondary/10 rounded-full flex items-center justify-center">
              <i class="fa fa-smile-o text-secondary text-xl"></i>
            </div>
          </div>
        </div>
        
        <div class="bg-white rounded-xl p-6 card-shadow">
          <div class="flex items-center justify-between">
            <div>
              <p class="text-gray-500 text-sm">焦虑比例</p>
              <h3 class="text-3xl font-bold mt-1 text-danger" id="anxiousPercentage">0%</h3>
            </div>
            <div class="w-12 h-12 bg-danger/10 rounded-full flex items-center justify-center">
              <i class="fa fa-frown-o text-danger text-xl"></i>
            </div>
          </div>
        </div>
      </div>
      
      <!-- 图表区域 -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 mb-8">
        <div class="bg-white rounded-xl p-6 card-shadow">
          <h3 class="text-lg font-semibold mb-4">情绪分布</h3>
          <div class="h-64">
            <canvas id="emotionPieChart"></canvas>
          </div>
        </div>
        
        <div class="bg-white rounded-xl p-6 card-shadow">
          <h3 class="text-lg font-semibold mb-4">近7天情绪趋势</h3>
          <div class="h-64">
            <canvas id="emotionTrendChart"></canvas>
          </div>
        </div>
      </div>
      
      <!-- 学生记录列表 -->
      <div class="bg-white rounded-xl p-6 card-shadow">
        <h3 class="text-lg font-semibold mb-4">今日学生情绪记录</h3>
        <div class="overflow-x-auto">
          <table class="min-w-full divide-y divide-gray-200">
            <thead>
              <tr>
                <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">学号</th>
                <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">姓名</th>
                <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">情绪状态</th>
                <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">备注</th>
                <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">记录时间</th>
              </tr>
            </thead>
            <tbody id="recordsTableBody" class="divide-y divide-gray-200">
              <tr>
                <td colspan="5" class="px-6 py-12 text-center text-gray-500">暂无记录</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>

    <!-- 学生账号查看弹窗（用于排查问题） -->
    <div id="studentsModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden">
      <div class="bg-white rounded-xl p-8 max-w-2xl w-full mx-4 max-h-[80vh] overflow-y-auto">
        <div class="flex justify-between items-center mb-6">
          <h3 class="text-xl font-bold">已导入学生账号</h3>
          <button id="closeStudentsModal" class="text-gray-500 hover:text-gray-700">
            <i class="fa fa-times text-xl"></i>
          </button>
        </div>
        <div class="overflow-x-auto">
          <table class="min-w-full divide-y divide-gray-200">
            <thead>
              <tr>
                <th class="px-4 py-3 text-left text-xs font-medium text-gray-500 uppercase">学号</th>
                <th class="px-4 py-3 text-left text-xs font-medium text-gray-500 uppercase">姓名</th>
                <th class="px-4 py-3 text-left text-xs font-medium text-gray-500 uppercase">密码</th>
              </tr>
            </thead>
            <tbody id="studentsTableBody" class="divide-y divide-gray-200">
              <tr>
                <td colspan="3" class="px-4 py-8 text-center text-gray-500">暂无学生账号</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>

    <!-- 提交成功提示 -->
    <div id="successModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden">
      <div class="bg-white rounded-xl p-8 max-w-md w-full mx-4 text-center">
        <div class="w-16 h-16 bg-secondary/10 rounded-full flex items-center justify-center mx-auto mb-6">
          <i class="fa fa-check text-secondary text-2xl"></i>
        </div>
        <h3 class="text-xl font-bold mb-2" id="successTitle">操作成功</h3>
        <p class="text-gray-600 mb-6" id="successMessage">操作已完成</p>
        <button id="closeSuccessModal" class="px-6 py-2 bg-primary text-white rounded-lg font-medium hover:bg-primary/90 transition-custom">
          确定
        </button>
      </div>
    </div>
  </main>

  <!-- 页脚 -->
  <footer class="bg-white border-t border-gray-200 py-6">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <p class="text-center text-gray-500 text-sm">
        &copy; 2023 学生情绪记录工具 | 辅导员专用系统
      </p>
    </div>
  </footer>

  <script>
    // 全局变量
    let currentUser = null;
    let emotionRecords = JSON.parse(localStorage.getItem('emotionRecords')) || [];
    let studentAccounts = JSON.parse(localStorage.getItem('studentAccounts')) || [];
    let counselorCredentials = JSON.parse(localStorage.getItem('counselorCredentials')) || {
      username: 'counselor',
      password: 'password123'
    };
    
    // 初始化日期显示
    function initDateDisplay() {
      const now = new Date();
      const options = { year: 'numeric', month: 'long', day: 'numeric', weekday: 'long' };
      document.getElementById('currentDate').textContent = now.toLocaleDateString('zh-CN', options);
    }
    
    // 页面切换函数
    function showPage(pageId) {
      // 隐藏所有页面
      document.getElementById('loginSelection').classList.add('hidden');
      document.getElementById('studentLogin').classList.add('hidden');
      document.getElementById('studentEmotionForm').classList.add('hidden');
      document.getElementById('studentChangePassword').classList.add('hidden');
      document.getElementById('counselorLogin').classList.add('hidden');
      document.getElementById('counselorDashboard').classList.add('hidden');
      document.getElementById('counselorChangePassword').classList.add('hidden');
      document.getElementById('studentsModal').classList.add('hidden');
      
      // 显示目标页面
      document.getElementById(pageId).classList.remove('hidden');
      
      if (pageId === 'counselorDashboard') {
        loadCounselorDashboard();
      }
    }
    
    // 【核心修复】学生登录验证逻辑（增加容错处理）
    document.getElementById('studentLoginForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const inputId = document.getElementById('studentId').value.trim(); // 去除输入的空格
      const inputPwd = document.getElementById('studentPassword').value.trim();
      
      // 1. 遍历所有学生账号，寻找匹配的学号（忽略前后空格）
      const matchedStudent = studentAccounts.find(student => {
        // 去除存储的学号中的空格后再比较
        const storedId = String(student.id).trim();
        return storedId === inputId;
      });
      
      // 2. 验证结果处理
      if (!matchedStudent) {
        alert(`未找到学号为【${inputId}】的学生，请检查学号是否正确或联系辅导员`);
        return;
      }
      
      // 3. 验证密码（忽略前后空格）
      const storedPwd = String(matchedStudent.password).trim();
      if (storedPwd !== inputPwd) {
        alert(`密码错误！学号【${inputId}】的初始密码为【${storedPwd}】，请核对后重试`);
        return;
      }
      
      // 4. 登录成功
      currentUser = {
        type: 'student',
        id: matchedStudent.id,
        name: matchedStudent.name
      };
      
      document.getElementById('displayStudentId').textContent = matchedStudent.id;
      document.getElementById('displayStudentName').textContent = matchedStudent.name;
      
      this.reset();
      showPage('studentEmotionForm');
    });
    
    // 辅导员登录
    document.getElementById('counselorLoginForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const username = document.getElementById('counselorUsername').value.trim();
      const password = document.getElementById('counselorPassword').value.trim();
      
      if (username === counselorCredentials.username && password === counselorCredentials.password) {
        currentUser = {
          type: 'counselor',
          username: username
        };
        showPage('counselorDashboard');
      } else {
        alert('用户名或密码错误');
      }
      
      this.reset();
    });
    
    // 提交情绪记录
    document.getElementById('emotionForm').addEventListener('submit', function(e) {
      e.preventDefault();
      
      if (!currentUser) {
        showPage('studentLogin');
        return;
      }
      
      const emotion = document.querySelector('input[name="emotion"]:checked').value;
      const notes = document.getElementById('notes').value;
      const now = new Date();
      
      const newRecord = {
        studentId: currentUser.id,
        studentName: currentUser.name,
        emotion: emotion,
        notes: notes,
        timestamp: now.toISOString(),
        date: now.toLocaleDateString()
      };
      
      const today = now.toLocaleDateString();
      const hasSubmittedToday = emotionRecords.some(record => 
        record.studentId === currentUser.id && record.date === today
      );
      
      if (hasSubmittedToday) {
        if (confirm('你今天已经提交过情绪记录了，是否要更新记录？')) {
          emotionRecords = emotionRecords.filter(record => 
            !(record.studentId === currentUser.id && record.date === today)
          );
          emotionRecords.push(newRecord);
          localStorage.setItem('emotionRecords', JSON.stringify(emotionRecords));
          showSuccessModal('提交成功', '你的情绪记录已更新');
        }
      } else {
        emotionRecords.push(newRecord);
        localStorage.setItem('emotionRecords', JSON.stringify(emotionRecords));
        showSuccessModal('提交成功', '感谢你的记录，祝你有美好的一天！');
      }
      
      this.reset();
    });
    
    // 学生修改密码
    document.getElementById('studentChangePwdForm').addEventListener('submit', function(e) {
      e.preventDefault();
      
      if (!currentUser || currentUser.type !== 'student') {
        showPage('studentLogin');
        return;
      }
      
      const oldPwd = document.getElementById('oldStudentPwd').value.trim();
      const newPwd = document.getElementById('newStudentPwd').value.trim();
      const confirmPwd = document.getElementById('confirmStudentPwd').value.trim();
      
      if (newPwd.length < 6) {
        alert('新密码长度至少为6位');
        return;
      }
      
      if (newPwd !== confirmPwd) {
        alert('两次输入的新密码不一致');
        return;
      }
      
      const studentIndex = studentAccounts.findIndex(s => String(s.id).trim() === String(currentUser.id).trim());
      if (studentIndex === -1) {
        alert('账号不存在');
        return;
      }
      
      if (String(studentAccounts[studentIndex].password).trim() !== oldPwd) {
        alert('原密码错误');
        return;
      }
      
      studentAccounts[studentIndex].password = newPwd;
      localStorage.setItem('studentAccounts', JSON.stringify(studentAccounts));
      
      this.reset();
      showSuccessModal('修改成功', '你的密码已更新，请使用新密码登录');
      showPage('studentLogin');
    });
    
    // 辅导员修改密码
    document.getElementById('counselorChangePwdForm').addEventListener('submit', function(e) {
      e.preventDefault();
      
      if (!currentUser || currentUser.type !== 'counselor') {
        showPage('counselorLogin');
        return;
      }
      
      const oldPwd = document.getElementById('oldCounselorPwd').value.trim();
      const newPwd = document.getElementById('newCounselorPwd').value.trim();
      const confirmPwd = document.getElementById('confirmCounselorPwd').value.trim();
      
      if (newPwd.length < 6) {
        alert('新密码长度至少为6位');
        return;
      }
      
      if (newPwd !== confirmPwd) {
        alert('两次输入的新密码不一致');
        return;
      }
      
      if (counselorCredentials.password !== oldPwd) {
        alert('原密码错误');
        return;
      }
      
      counselorCredentials.password = newPwd;
      localStorage.setItem('counselorCredentials', JSON.stringify(counselorCredentials));
      
      this.reset();
      showSuccessModal('修改成功', '密码已更新，请使用新密码登录');
      showPage('counselorLogin');
    });
    
    // 显示成功提示框
    function showSuccessModal(title, message) {
      document.getElementById('successTitle').textContent = title;
      document.getElementById('successMessage').textContent = message;
      document.getElementById('successModal').classList.remove('hidden');
    }
    
    // 关闭成功提示
    document.getElementById('closeSuccessModal').addEventListener('click', function() {
      document.getElementById('successModal').classList.add('hidden');
    });
    
    // 【核心修复】导入学生账号时自动去除空格
    document.getElementById('importStudents').addEventListener('click', function() {
      const fileInput = document.getElementById('studentFile');
      const file = fileInput.files[0];
      
      if (!file) {
        alert('请选择Excel或CSV文件');
        return;
      }
      
      const fileExtension = file.name.split('.').pop().toLowerCase();
      if (!['xlsx', 'xls', 'csv'].includes(fileExtension)) {
        alert('请选择Excel或CSV格式的文件');
        return;
      }
      
      const reader = new FileReader();
      reader.onload = function(e) {
        try {
          const data = new Uint8Array(e.target.result);
          const workbook = XLSX.read(data, { type: 'array' });
          const firstSheet = workbook.Sheets[workbook.SheetNames[0]];
          const students = XLSX.utils.sheet_to_json(firstSheet);
          
          // 导入时自动去除学号、姓名、密码中的前后空格
          const newAccounts = students.map((s, index) => {
            return {
              id: String(s.学号 || s.studentId || s.id || `temp_${index + 1}`).trim(),
              name: String(s.姓名 || s.studentName || s.name || `未知姓名_${index + 1}`).trim(),
              password: String(s.密码 || s.pwd || s.password || '123456').trim() // 默认密码
            };
          }).filter(s => s.id && s.name); // 过滤空数据
          
          if (newAccounts.length === 0) {
            alert('未识别到有效学生数据，请检查文件格式');
            return;
          }
          
          // 合并账号列表（去重）
          const existingIds = new Set();
          const mergedAccounts = [...newAccounts, ...studentAccounts].filter(s => {
            const trimmedId = String(s.id).trim();
            if (existingIds.has(trimmedId)) return false;
            existingIds.add(trimmedId);
            return true;
          });
          
          // 保存到本地存储
          studentAccounts = mergedAccounts;
          localStorage.setItem('studentAccounts', JSON.stringify(studentAccounts));
          
          // 更新显示
          document.getElementById('studentCount').textContent = `当前学生账号数量：${studentAccounts.length}人`;
          showSuccessModal('导入成功', `成功导入 ${newAccounts.length} 个学生账号，当前总数量：${studentAccounts.length}人`);
          
          // 清空文件选择
          fileInput.value = '';
        } catch (error) {
          console.error('导入失败', error);
          alert('文件解析失败，请检查文件格式是否正确');
        }
      };
      reader.readAsArrayBuffer(file);
    });
    
    // 导出学生账号
    document.getElementById('exportStudents').addEventListener('click', function() {
      if (studentAccounts.length === 0) {
        alert('没有可导出的学生账号数据');
        return;
      }
      
      const exportData = studentAccounts.map(s => ({
        学号: s.id,
        姓名: s.name,
        密码: s.password
      }));
      
      const worksheet = XLSX.utils.json_to_sheet(exportData);
      const workbook = XLSX.utils.book_new();
      XLSX.utils.book_append_sheet(workbook, worksheet, '学生账号');
      
      const today = new Date().toLocaleDateString().replace(/\//g, '-');
      XLSX.writeFile(workbook, `学生账号_${today}.xlsx`);
    });
    
    // 【新增功能】查看已导入的学生账号（用于排查登录问题）
    document.getElementById('checkStudents').addEventListener('click', function() {
      const tableBody = document.getElementById('studentsTableBody');
      tableBody.innerHTML = '';
      
      if (studentAccounts.length === 0) {
        tableBody.innerHTML = '<tr><td colspan="3" class="px-4 py-8 text-center text-gray-500">暂无学生账号</td></tr>';
        document.getElementById('studentsModal').classList.remove('hidden');
        return;
      }
      
      // 显示所有学生账号（包含密码，方便核对）
      studentAccounts.forEach(student => {
        const row = document.createElement('tr');
        row.innerHTML = `
          <td class="px-4 py-3 whitespace-nowrap">${student.id}</td>
          <td class="px-4 py-3 whitespace-nowrap">${student.name}</td>
          <td class="px-4 py-3 whitespace-nowrap font-mono text-sm">${student.password}</td>
        `;
        tableBody.appendChild(row);
      });
      
      document.getElementById('studentsModal').classList.remove('hidden');
    });
    
    // 关闭学生账号查看弹窗
    document.getElementById('closeStudentsModal').addEventListener('click', function() {
      document.getElementById('studentsModal').classList.add('hidden');
    });
    
    // 加载辅导员仪表盘数据
    function loadCounselorDashboard() {
      document.getElementById('studentCount').textContent = `当前学生账号数量：${studentAccounts.length}人`;
      
      const today = new Date().toLocaleDateString();
      const todayRecords = emotionRecords.filter(record => record.date === today);
      
      const totalStudents = new Set(todayRecords.map(record => record.studentId)).size;
      const happyCount = todayRecords.filter(record => record.emotion === '开心').length;
      const neutralCount = todayRecords.filter(record => record.emotion === '平淡').length;
      const anxiousCount = todayRecords.filter(record => record.emotion === '有点焦虑').length;
      
      const happyPercentage = totalStudents > 0 ? Math.round((happyCount / totalStudents) * 100) : 0;
      const anxiousPercentage = totalStudents > 0 ? Math.round((anxiousCount / totalStudents) * 100) : 0;
      
      document.getElementById('totalStudents').textContent = totalStudents;
      document.getElementById('happyPercentage').textContent = `${happyPercentage}%`;
      document.getElementById('anxiousPercentage').textContent = `${anxiousPercentage}%`;
      
      updateRecordsTable(todayRecords);
      drawEmotionPieChart(happyCount, neutralCount, anxiousCount);
      drawEmotionTrendChart();
    }
    
    // 更新记录表格
    function updateRecordsTable(records) {
      const tableBody = document.getElementById('recordsTableBody');
      tableBody.innerHTML = '';
      
      if (records.length === 0) {
        const row = document.createElement('tr');
        row.innerHTML = '<td colspan="5" class="px-6 py-12 text-center text-gray-500">暂无记录</td>';
        tableBody.appendChild(row);
        return;
      }
      
      records.sort((a, b) => new Date(b.timestamp) - new Date(a.timestamp));
      
      records.forEach(record => {
        const row = document.createElement('tr');
        
        let emotionClass = '';
        let emotionText = '';
        
        switch(record.emotion) {
          case '开心':
            emotionClass = 'bg-secondary/10 text-secondary';
            emotionText = '开心';
            break;
          case '平淡':
            emotionClass = 'bg-warning/10 text-warning';
            emotionText = '平淡';
            break;
          case '有点焦虑':
            emotionClass = 'bg-danger/10 text-danger';
            emotionText = '有点焦虑';
            break;
        }
        
        const time = new Date(record.timestamp).toLocaleTimeString();
        
        row.innerHTML = `
          <td class="px-6 py-4 whitespace-nowrap">${record.studentId}</td>
          <td class="px-6 py-4 whitespace-nowrap">${record.studentName}</td>
          <td class="px-6 py-4 whitespace-nowrap">
            <span class="px-2 py-1 text-xs font-medium rounded-full ${emotionClass}">${emotionText}</span>
          </td>
          <td class="px-6 py-4">${record.notes || '-'}</td>
          <td class="px-6 py-4 whitespace-nowrap text-gray-500">${time}</td>
        `;
        
        tableBody.appendChild(row);
      });
    }
    
    // 绘制情绪分布饼图
    function drawEmotionPieChart(happy, neutral, anxious) {
      const ctx = document.getElementById('emotionPieChart').getContext('2d');
      
      if (window.emotionPieChartInstance) {
        window.emotionPieChartInstance.destroy();
      }
      
      window.emotionPieChartInstance = new Chart(ctx, {
        type: 'doughnut',
        data: {
          labels: ['开心', '平淡', '有点焦虑'],
          datasets: [{
            data: [happy, neutral, anxious],
            backgroundColor: ['#10B981', '#F59E0B', '#EF4444'],
            borderWidth: 0
          }]
        },
        options: {
          responsive: true,
          maintainAspectRatio: false,
          plugins: { legend: { position: 'bottom' } },
          cutout: '65%'
        }
      });
    }
    
    // 绘制近7天情绪趋势图
    function drawEmotionTrendChart() {
      const ctx = document.getElementById('emotionTrendChart').getContext('2d');
      
      if (window.emotionTrendChartInstance) {
        window.emotionTrendChartInstance.destroy();
      }
      
      const dates = [];
      const happyData = [];
      const neutralData = [];
      const anxiousData = [];
      
      for (let i = 6; i >= 0; i--) {
        const date = new Date();
        date.setDate(date.getDate() - i);
        const dateStr = date.toLocaleDateString();
        const dateLabel = date.getMonth() + 1 + '/' + date.getDate();
        
        dates.push(dateLabel);
        
        const dayRecords = emotionRecords.filter(record => record.date === dateStr);
        happyData.push(dayRecords.filter(r => r.emotion === '开心').length);
        neutralData.push(dayRecords.filter(r => r.emotion === '平淡').length);
        anxiousData.push(dayRecords.filter(r => r.emotion === '有点焦虑').length);
      }
      
      window.emotionTrendChartInstance = new Chart(ctx, {
        type: 'line',
        data: {
          labels: dates,
          datasets: [
            {
              label: '开心',
              data: happyData,
              borderColor: '#10B981',
              backgroundColor: 'rgba(16, 185, 129, 0.1)',
              tension: 0.3,
              fill: true
            },
            {
              label: '平淡',
              data: neutralData,
              borderColor: '#F59E0B',
              backgroundColor: 'rgba(245, 158, 11, 0.1)',
              tension: 0.3,
              fill: true
            },
            {
              label: '有点焦虑',
              data: anxiousData,
              borderColor: '#EF4444',
              backgroundColor: 'rgba(239, 68, 68, 0.1)',
              tension: 0.3,
              fill: true
            }
          ]
        },
        options: {
          responsive: true,
          maintainAspectRatio: false,
          plugins: { legend: { position: 'bottom' } },
          scales: { y: { beginAtZero: true, ticks: { precision: 0 } } }
        }
      });
    }
    
    // 事件监听器 - 导航和页面切换
    document.getElementById('studentLoginBtn').addEventListener('click', () => showPage('studentLogin'));
    document.getElementById('counselorLoginBtn').addEventListener('click', () => showPage('counselorLogin'));
    document.getElementById('studentCard').addEventListener('click', () => showPage('studentLogin'));
    document.getElementById('counselorCard').addEventListener('click', () => showPage('counselorLogin'));
    document.getElementById('backFromStudentLogin').addEventListener('click', () => showPage('loginSelection'));
    document.getElementById('backFromCounselorLogin').addEventListener('click', () => showPage('loginSelection'));
    document.getElementById('backToEmotionForm').addEventListener('click', () => showPage('studentEmotionForm'));
    document.getElementById('backToDashboard').addEventListener('click', () => showPage('counselorDashboard'));
    
    // 修改密码相关按钮
    document.getElementById('studentChangePwdBtn').addEventListener('click', () => showPage('studentChangePassword'));
    document.getElementById('counselorChangePwdBtn').addEventListener('click', () => showPage('counselorChangePassword'));
    
    // 退出登录
    document.getElementById('studentLogout').addEventListener('click', function() {
      currentUser = null;
      showPage('loginSelection');
    });
    
    document.getElementById('counselorLogout').addEventListener('click', function() {
      currentUser = null;
      showPage('loginSelection');
    });
    
    // 页面滚动时改变导航栏样式
    window.addEventListener('scroll', function() {
      const nav = document.querySelector('nav');
      if (window.scrollY > 10) {
        nav.classList.add('shadow-lg');
        nav.classList.remove('shadow-md');
      } else {
        nav.classList.remove('shadow-lg');
        nav.classList.add('shadow-md');
      }
    });
    
    // 初始化
    function init() {
      initDateDisplay();
      showPage('loginSelection');
    }
    
    // 页面加载完成后初始化
    window.addEventListener('DOMContentLoaded', init);
  </script>
</body>
</html>
