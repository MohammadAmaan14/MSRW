<p align="center">
  <img src="https://forthebadge.com/images/badges/made-with-python.svg"/>
  <img src="http://ForTheBadge.com/images/badges/built-by-developers.svg"/>
  <img src="http://ForTheBadge.com/images/badges/uses-git.svg"/>
  <img src="http://ForTheBadge.com/images/badges/built-with-love.svg"/>
</p>

<pre align="center">
███╗   ███╗███████╗    ███████╗ █████╗ ██████╗ ███╗   ███╗███████╗██████╗ 
████╗ ████║██╔════╝    ██╔════╝██╔══██╗██╔══██╗████╗ ████║██╔════╝██╔══██╗
██╔████╔██║███████╗    █████╗  ███████║██████╔╝██╔████╔██║█████╗  ██████╔╝
██║╚██╔╝██║╚════██║    ██╔══╝  ██╔══██║██╔══██╗██║╚██╔╝██║██╔══╝  ██╔══██╗
██║ ╚═╝ ██║███████║    ██║     ██║  ██║██║  ██║██║ ╚═╝ ██║███████╗██║  ██║
╚═╝     ╚═╝╚══════╝    ╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝     ╚═╝╚══════╝╚═╝  ╚═╝
        built by @farshadz1997 upgraded by @Ghosty-Gigabytes      version 3.2
</pre>

<p align="center">
  <img src="https://img.shields.io/badge/Maintained%3F-yes-green.svg?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge"/>
</p>

<h2 align="center">👋 Welcome to the future of automation</h2>
<h3 align="center">A simple bot that uses selenium to farm Microsoft Rewards written in Python.</h3>

<h2 align="center">Installation</h2>
<p allign="center">You can also find this repository on <a href="https://gitlab.com/farshadzargary1997/Microsoft-Rewards-bot">Gitlab</a>.</p>
<p align="center">
  <ul>
    <li>Install requirements with the following command : <pre>pip install -r requirements.txt</pre></li>
    <li>Make sure you have Chrome installed</li>
    <li>Install ChromeDriver :<ul>
      <li>Windows :<ul>
        <li>Download Chrome WebDriver as same as your Google Chrome version : https://chromedriver.chromium.org/downloads</li>
        <li>Place the file in X:\Windows (X as your Windows disk letter)</li>
      </ul>
      <li>MacOS or Linux :<ul>
        <li><pre>apt install chromium-chromedriver</pre></li>
        <li>or if you have brew : <pre>brew cask install chromedriver</pre></li>
      </ul>
    </ul></li>
   <li>Edit the accounts.json.sample with your accounts credentials and rename it by removing <code>.sample</code> at the end.<br/>
    If you want to add more than one account, the syntax is the following (<code>mobile_user_agent</code>, <code>proxy</code> and <code>goal</code> are optional).
    Remove <code>mobile_user_agent</code>, <code>proxy</code> or <code>goal</code> from your account if you don't know how to use them:<pre>[{
        "username": "Your Email",
        "password": "Your Password",
        "mobile_user_agent": "your preferred mobile user agent",
        "proxy": "HTTP proxy",
        "goal": "Amazon"
    },
    {
        "username": "Your Email 2",
        "password": "Your Password 2",
        "mobile_user_agent": "your preferred mobile user agent",
        "proxy": "HTTP proxy",
        "goal": "Xbox Game Pass Ultimate"
}]</pre></li>
    <li>Enter your telegram bot credentials in the msr.py : <pre>TOKEN_TELEGRAM = 'X' #Telegram token id replace X
CHAT_ID_TELEGRAM = '-X' #Telegram Chat ID replace X, don't remove hypen</pre></li>
    <li>Name your Nodes using this (useful if you would run multiple copies of the script at the same time, just an identifer number for all the copies) : <pre>Local_NODE = '1'</pre></li>
    <li>Due to limits of Ipapi sometimes it returns error and it causes bot stops. So you can define default language and location to prevent it from 
      <a href="https://github.com/farshadz1997/Microsoft-Rewards-bot/blob/479b2d4b25761d245dc6b3519627162a44d8f85b/ms_rewards_farmer.py#L367">here</a>.</li>
    <li>Run the script</li>
      <ul>
        <li>Use optinal arguments</li>
          <ul>
            <li><code>--headless</code> You can use this argument to run the script in headless mode.</li>
            <li><code>--redeem</code> Enable auto-redeem rewards based on accounts.json goals.</li>
            <li><code>--calculator</code> Opens GUI calculator with custom options. When using this flag the script will not run.</li>
            <li><code>--session</code> Use this argument to create session for each account.</li>
            <li><code>--fast</code> This argument reduces delays of script and make it faster (use this if you have high speed connection).</li>
            <li><code>--superfast</code> This argument is faster than fast (use this if you have a very high speed and reliable connection).</li>            
            <li><code>--account-browser ACCOUNT</code> This argument opens session for given account if it's already exist else returns error.</li>
            <li><code>--error</code> When you use this argument, app displays crash error in terminal when it fails.</li>
            <li><code>--NOtelegram</code> Use this argument to disable sending logs to your telegram through your bot.</li>
            <li><code>--discord WEBHOOK_URL</code> Use this argument to send logs to your Discord server through webhook.</li>
            <li><code>--skip-unusual</code> Click on skip for 5 days on unusual activity detection.</li>
            <li><code>--edge</code> Use Microsoft Edge webdriver instead of Chrome.<a href="https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/"> Download Microsoft Edge web driver.</a></li>
            <li><code>--on-finish ACTION</code> Action to perform on finish from one of the following: shutdown, sleep, hibernate, exit.</li>
            <li><code>--skip-shopping</code> Skips MSN shopping game.</li>
            <li>For example type in your terminal <code>python ms_rewards_farmer.py --slow --session</code> You don't need to use all of arguments.</li>
          </ul>
        <li>Run the script normally that session and headless disabled and it asks you to input a time if you want to run it at a specific time.</li>
      </ul>
   </ul>
</p>

<h2 align="center">Features</h2>
<p align="center">
<ul>
  <li>Bing searches (Desktop, Mobile and Edge) with User-Agents</li>
  <li>Complete automatically the daily set</li>
  <li>Complete automatically punch cards</li>
  <li>Complete automatically the others promotions</li>
  <li>Complete MSN shopping game quiz</li>
  <li>Headless Mode</li>
  <li>Multi-Account Management</li>
  <li>If it faces to an unexpected error then try the account from first</li>  
  <li>Save progress of bot in a log file and use it to pass completed account on the next start at the same day</li>
  <li>Detect suspended accounts</li>
  <li>Detect locked accounts</li>
  <li>Detect unusual activities</li>
  <li>Uses time out to prevent infinite loop</li>
  <li>You can assign custom user-agent for mobile like above example</li>
  <li>Set clock to start it at specific time</li>
  <li>For Bing search it uses random word at first try and if api failed then it uses google trends</li>
  <li>Support HTTP proxy</li>
  <li>Auto-redeem rewards</li>
  <li>Rewards Calculator </li>
</ul>
<h2 align="center">AUTO-REDEEM (BETA)</h2>
<p align="left">
  <h4 align="left">This feature is still in beta! Feel free to try it and report any problems you find. Bear in mind that this feature was designed, so it would only redeem one card from one account each time you run the farmer. This is intentional so your accounts are less likely to get banned. If you do not specify any goal in accounts.json, it will default to Amazon Gift Cards</h4>
<br>
<h2 align="center">⚠️CAUTION!⚠️</h2>
<p align="center">
  <h4 align="center">Do not use headless mode, it can cause your account to be suspended from Microsoft Rewards.</h4>
