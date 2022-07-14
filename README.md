
from selenium import webdriver
import time
from selenium.webdriver.common.by import By

class Guvi:
    url ="https://www.zenclass.in/login"
    driver=webdriver.Chrome()


    def test(self):
        Email = "santhoshnitesh@gmail.com"
        Password = "Santhosh123@."
        self.driver.get(self.url)
        time.sleep(5)

   
        username_xpath = '//*[@name="email"]'
        password_xpath = '//*[@name="password"]'
        submit_button_xpath = '//*[@type="submit"]'
        time.sleep(5)
        
#email id & password path & button    
        Username = self.driver.find_element(by=By.XPATH, value=username_xpath)
        password = self.driver.find_element(by=By.XPATH, value=password_xpath)
        submit_button = self.driver.find_element(by=By.XPATH, value=submit_button_xpath)

        Username.send_keys(Email)
        password.send_keys(Password)
        submit_button.click()
        time.sleep(5)
        
    # Created Method to create queries
    def query_button(self):
        Main_Heading = 'Guvi Python AT – 1 &2 Automation Project'
        Main_Description = 'This is a Project Test Code Running for the Python Automation – 1&2 Project Given by mentor Mr. Suman Gangopadhyay'

        

        query_button: str = '//*[@id="root"]/div[1]/nav/ul/div[6]/li/span/div/div[2]'
        query_button_1 = self.driver.find_element(by=By.XPATH, value=query_button)
        query_button_1.click()
        time.sleep(3)


        Main: str = ' // *[@ id = "root"] / nav'
        just1 = self.driver.find_element(by=By.XPATH, value = Main)
        just1.click()
        time.sleep(3)
        

        
        query_button_2 = '/html/body/div/div[2]/div/div[1]/div[1]/button'
        query_button_2 = self.driver.find_element(by=By.XPATH, value = query_button_2)
        query_button_2.click()
        time.sleep(4)
        

        cancel_button = '/html/body/div/div[2]/div/div[2]/div[6]/div[2]/div/div/section[3]/div[2]/button[1]'
        cancel_button_1 = self.driver.find_element(by=By.XPATH, value=cancel_button)
        cancel_button_1.click()
        time.sleep(4)
       

        
        category_button ='/html/body/div/div[2]/div/div[2]/div/div/form/div[2]/div[1]/select/option[3]'
        category_button_1 =self.driver.find_element(by=By.XPATH, value=category_button)
        category_button_1.click()
        time.sleep(3)
      

       
        prefer_Language = '/html/body/div/div[2]/div/div[2]/div/div/form/div[2]/div[2]/select/option[3]'
        prefer_Language_2 = self.driver.find_element(by=By.XPATH, value=prefer_Language)
        prefer_Language_2.click()
        time.sleep(3)
       

      
        Query_title = '/html/body/div/div[2]/div/div[2]/div/div/form/div[5]/div/input'
        Query_title_3 = self.driver.find_element(by=By.XPATH, value=Query_title)
        Query_title_3.send_keys(Main_Heading)
        time.sleep(4)
        

       
        Query_Description = '/html/body/div/div[2]/div/div[2]/div/div/form/div[5]/textarea'
        Query_Description_4 = self.driver.find_element(by=By.XPATH, value=Query_Description)
        Query_Description_4.send_keys(Main_Description)
        time.sleep(3)
        

        
        Submit_Button = '/html/body/div/div[2]/div/div[2]/div/div/form/div[13]/div/button'
        submit_Button_1 = self.driver.find_element(by=By.XPATH, value=Submit_Button)
        submit_Button_1.click()
      





N = Guvi()
N.test()
N.query_button()

