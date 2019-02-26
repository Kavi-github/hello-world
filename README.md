# hello-world
First Sample project
Adding few more contents to this file to make differ from master repository
package Selenium;

import java.util.concurrent.TimeUnit;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class flipkart {

	public static void main(String[] args) throws InterruptedException {
	
		System.setProperty("webdriver.chrome.driver","C:\\Users\\ka342896\\Downloads\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();

		driver.get("http://facebook.com");
		 driver.manage().window().maximize();
	
		
		driver.findElement(By.xpath("//input[contains(@data-testid,'royal_email')]")).sendKeys("kaviyamudhu@gmail.com");
		driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
		driver.findElement(By.xpath("//input[contains(@data-testid,'royal_pass')]")).sendKeys("KaviPriyan");
		driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
		driver.findElement(By.xpath("//input[contains(@value,'Log In')]")).click();
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
	
		driver.quit();
	}
	
}
