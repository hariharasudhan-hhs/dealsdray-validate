package deals;
import java.time.Duration;
import java.util.concurrent.TimeUnit;

import org.openqa.selenium. *;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.Keys;

public class Validate {

	public static void main(String[] args) throws Exception {
		ScreenRecorderUtil.startRecord("main");
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.navigate().to("https://demo.dealsdray.com/");
		driver.findElement(By.name("username")).sendKeys("prexo.mis@dealsdray.com");
		driver.findElement(By.name("password")).sendKeys("prexo.mis@dealsdray.com");
		driver.manage().timeouts().implicitlyWait(15,TimeUnit.SECONDS);
		driver.findElement(By.xpath("/html/body/div/div/div/div/div[2]/div/form/div[3]/div/button")).click();
		driver.findElement(By.xpath("/html/body/div/div/div[1]/div/div[2]/div[1]/div[2]/button")).click();
		driver.findElement(By.xpath("/html/body/div/div/div[1]/div/div[2]/div[1]/div[2]/div/div[1]/a/button/span[1]")).click();
		driver.findElement(By.xpath("/html/body/div/div/div/div[2]/div/div/div[2]/div[2]/button")).click();
		driver.findElement(By.xpath("/html/body/div/div/div/div[2]/div/div/div[2]/div[3]/div/div/input")).sendKeys("C:\\Users\\harih\\Downloads\\demo-data.xlsx");
		driver.findElement(By.xpath("/html/body/div/div/div/div[2]/div/div/div[2]/div[3]/button")).click();
		driver.findElement(By.xpath("/html/body/div/div/div/div[2]/div/div/div[2]/div[3]/button")).click();
		driver.manage().timeouts().implicitlyWait(10,TimeUnit.SECONDS);
		ScreenRecorderUtil.stopRecord();		
	}

}
