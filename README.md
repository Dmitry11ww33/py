# py
from selenium import webdriver
from selenium.common import NoSuchElementException
from selenium.webdriver.common.by import By
#
driver = webdriver.Chrome()
driver.get("https://ru.wikipedia.org/wiki/%D0%9A%D0%BE%D1%88%D0%BA%D0%B0")
# try:
#    elem = driver.find_element(By.ID, "searchInput")
#    print('Элемент нашелся')
# except NoSuchElementException:
#    print(":(")
#driver.close()

# ------------By.TAG_NAME-------------#
try:
   elements = driver.find_elements(By.TAG_NAME, "p")
   print(elements, len(elements))
   for element in elements:
      print(element.text, '\n\n----------------------\n\n')
except NoSuchElementException:
   print("нет ни одного элемента")
