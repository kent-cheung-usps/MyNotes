# MyNotes
Simply personal technical note

## Sample Code
```
package testcases;
 
import java.nio.file.Paths;
 
import com.microsoft.playwright.Browser;
import com.microsoft.playwright.BrowserContext;
import com.microsoft.playwright.BrowserType;
import com.microsoft.playwright.Page;
import com.microsoft.playwright.Page.GoBackOptions;
import com.microsoft.playwright.Page.GoForwardOptions;
import com.microsoft.playwright.Playwright;
import com.microsoft.playwright.Tracing;
 
public class NonIncognitoWindowTest {
 
	public static void main(String[] args) throws InterruptedException { 
	Playwright playwright = Playwright.create();
	Browser browser = playwright.chromium().launch(new BrowserType.LaunchOptions().setHeadless(false));
		
	BrowserContext browserContext = playwright.chromium().launchPersistentContext(Paths.get("C:\\Users\\way2automation\\AppData\\Local\\Google\\Chrome\\User Data\\Default"), new BrowserType.LaunchPersistentContextOptions().setHeadless(false).setExecutablePath(Paths.get("C:\\Program Files\\Google\\Chrome\\Application\\chrome.exe")));
 		
	Page page = browserContext.newPage();
	page.navigate("http://way2automation.com");
	System.out.println(page.title());
		
	page.navigate("http://google.com");
	page.goBack(new GoBackOptions().setTimeout(500));
	Thread.sleep(1000);
	page.goForward(new GoForwardOptions().setTimeout(500));
	Thread.sleep(1000);

	page.reload();
	page.close();
	browserContext.close();
	playwright.close();
	}
}
```
## Mazimizing the windows - Code by width and height
```
Dimension screenSize = Toolkit.getDefaultToolkit().getScreenSize();
double width = screenSize.getWidth();
double height = screenSize.getHeight();
		
System.out.println(width+"---"+height);
		
Playwright playwright = Playwright.create();
Browser browser = playwright.chromium().launch(new BrowserType.LaunchOptions().setHeadless(false));
		
BrowserContext browserContext = browser.newContext(new Browser.NewContextOptions().setViewportSize((int)width, (int)height));
Page page = browserContext.newPage();
page.navigate("http://way2automation.com");
System.out.println(page.title());
Thread.sleep(2000);
//page.close();
//playwright.close();
```

## Another simple way of Maximizing the window - Code
```
package testcases;
import java.util.ArrayList;
import com.microsoft.playwright.Browser;
import com.microsoft.playwright.BrowserContext;
import com.microsoft.playwright.BrowserType;
import com.microsoft.playwright.Page;
import com.microsoft.playwright.Playwright;
 
public class MaximizingWindow {
 
	public static void main(String[] args) {
    Playwright playwright = Playwright.create();
		ArrayList<String> arguments = new ArrayList<>();
		arguments.add("--start-maximized");
		Browser browser = playwright.chromium().launch(new BrowserType.LaunchOptions().setChannel("chrome").setHeadless(false).setArgs(arguments));
		BrowserContext context = browser.newContext(new Browser.NewContextOptions().setViewportSize(null));
		
		Page page = context.newPage();
 
		page.navigate("http://way2automation.com");
		System.out.println(page.title());
	}
}
```
