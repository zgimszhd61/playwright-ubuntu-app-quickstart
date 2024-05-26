# playwright-ubuntu-app-quickstart
Playwright 是一个开源的自动化测试工具，支持多种编程语言，可以在 Ubuntu 系统中安装和运行。以下是一个使用 JavaScript 和 Node.js 在 Ubuntu 上安装 Playwright 并运行一个简单测试的例子。

首先，确保你的系统已经安装了 Node.js。你可以通过运行以下命令来检查 Node.js 是否已安装：

```bash
node --version
```

如果没有安装 Node.js，你可以通过 [Node.js 官网](https://nodejs.org/) 或使用 Ubuntu 的包管理器 `apt` 来安装。以下是使用 `apt` 安装 Node.js 的命令：

```bash
sudo apt update
sudo apt install nodejs
sudo apt install npm
```

安装完 Node.js 和 npm 后，你可以创建一个新的项目文件夹并初始化一个新的 Node.js 项目：

```bash
mkdir playwright-test
cd playwright-test
npm init -y
```

接下来，安装 Playwright 到你的项目中：

```bash
npm i -D @playwright/test
```

安装完成后，创建一个名为 `example.spec.js` 的测试文件，并添加以下代码：

```javascript
// example.spec.js
const { test, expect } = require('@playwright/test');

test('basic test', async ({ page }) => {
  await page.goto('https://playwright.dev/');
  const title = await page.title();
  expect(title).toBe('Fast and reliable end-to-end testing for modern web apps | Playwright');
});
```

这段代码会打开 Playwright 的官方网站，并检查页面标题是否正确。

最后，运行测试：

```bash
npx playwright test
```

如果一切设置正确，你应该会看到测试通过的信息。

以上就是在 Ubuntu 上使用 Playwright 进行自动化测试的一个简单例子。Playwright 支持 Chromium、Firefox 和 WebKit，因此你可以在多个浏览器上运行相同的测试[7][13]。

Citations:
[1] https://github.com/microsoft/playwright/issues/23296
[2] https://github.com/microsoft/playwright/issues/11122
[3] https://brahmakothapalli.hashnode.dev/playwright-02-installing-playwright-using-nodejs-and-vs-code
[4] https://github.com/microsoft/playwright-examples
[5] https://blog.openreplay.com/testing-with-playwright/
[6] https://saucelabs.com/resources/blog/getting-started-with-playwright-testing
[7] https://github.com/microsoft/playwright
[8] https://playwright.dev/docs/writing-tests
[9] https://www.browserstack.com/guide/playwright-tutorial
[10] https://testguild.com/playwright-tutorial-getting-started-with-playwright-framework/
[11] https://playwright.dev/python/docs/intro
[12] https://playwright.dev/docs/best-practices
[13] https://playwright.dev/docs/intro
[14] https://playwright.dev/dotnet/docs/intro
[15] https://playwright.bootcss.com/docs/installation
[16] https://testgrid.io/blog/playwright-installation-guide/
