from selenium import webdriver
import math
import time

try:
    browser = webdriver.Chrome()
    browser.get('http://suninjuly.github.io/find_link_text')
    browser.find_element_by_link_text(str(math.ceil(math.pow(math.pi, math.e)*10000))).click()
    browser.find_element_by_tag_name('input').send_keys("Ivan")
    browser.find_element_by_name('last_name').send_keys("Petrov")
    browser.find_element_by_class_name('city').send_keys("Smolensk")
    browser.find_element_by_id('country').send_keys("Russia")
    browser.find_element_by_css_selector("button.btn").click()

finally:
    time.sleep(30)
    browser.quit()