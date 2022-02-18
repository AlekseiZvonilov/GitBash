**1)Посмотреть где я**  
* pwd  
     
**2)Создать папку**   
* mkdir folder  
  
**3)Зайти в папку**    
* cd folder  
* cd /c/Users/hp/OneDrive/Документы/GHHW_27Group/folder - полный путь
    
**4)Создать 3 папки**    
* mkdir folder1 folder2 folder3    
* mkdir folder{1..3} - или так     
* mkdir -p folder/filder1/folder2 - папки будут вложены одна в другую поочередно  
     
**5)Зайти в любую папку**     
* cd folder1    
   
**6)Создать 5 файлов (3 txt, 2 json)**       
* touch {file1.txt,file2.txt,file3.txt,file1.json,file2.json}      
* touch file{1..3}.txt file{1..2}.json - или так      
* touch file1.txt file2.txt file3.txt file1.json file2.json - или так   
     
**7)Создать 3 папки**        
* mkdir folder_1 folder_2 folder_3      
* mkdir folder_{1..3} - или так 
      
**8)Вывести список содержимого папки**        
* ls      
* ls -aF - вы ведет список и тип файлов    
* ls -lt - с сортировкой по дате      
* ls -lu - с сортировкой по дате обращения       
* ls -la - вывод всех файлов с датой, размером, расширением, владельцем   
             
**9)Открыть любой txt файл**            
* vim file1.txt   
               
**10)Написать туда что-нибудь, любой текст**                          
* i - редакторование  (quality assurance quality control)  
                              
**11)Сохранить и выйти**                           
* ecs - выйти из редактирования                     
* :wq - сохранить и выйти   
                         
**12)Выйти из папки на уровень выше**                            
* cd ..                       
* cd ../.. - на 2 уровня выше    
                             
**13)Переместить любые 2 файла, которые вы создали, в любую другую папку**                                
* mv folder1/{file1.txt,file1.json} folder1/folder_1 
                        
**14)Скопировать любые 2 файла, которые вы создали, в любую другую папку**                         
* cp folder1/{file2.txt,file2.json} folder1/folder_2 
                    
**15)Найти файл по имени**                                                
* find . -name "file2.json"  
                          
**16)Посмотреть содержимаое в реальном времени (команда grep)**                                
* tail -f folder1/folder_1/file1.txt | grep quality  
                    
**17)Вывести несколько первых строк из текстового файла**                        
* head -2 folder1/folder_1/file1.txt   
                    
**18)Вывести несколько последних строк из текстового файла**                     
* tail -2 folder1/folder_1/file1.txt   
                    
**19)Посмотреть содержимое длинного файла (команда less)**                     
* less folder1/folder_1/file1.txt                             
* q - выйти из режима просмотра   
                                       
**20)Вывести дату и время**                                
* date                       
                 
Задание*                                   
**1)Отправить http запрос на сервер. http://162.55.220.72:5005/terminal-hw-request**                     
* curl "http://162.55.220.72:5005/terminal-hw-request"                              
Ответ сервера{"Intro":"Hello!! This is your the first response from server","Tasks":{"Task_1":"Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)","result":["Your_String","Your_number"]}}                
* Task1           
* curl "http://162.55.220.72:5005/get_method?name=(Zvonilov)&age=(33)"                     
В ответе сервера изменяем (set_your_String) - Имя, (set_your_number) - возраст                     
Ответ сервера ["(Zvonilov)","(33)"]   
                
**2)Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13 (добавил пункты 1 и 2 для запуска файла script из любой папки)**                 
```       
cat > script.sh << EOF              
#!/bin/bash                        
pwd                 
mkdir script_folder         
cd script_folder                           
mkdir folder1 folder2 folder3                          
cd folder1               
touch {file1.txt,file2.txt,file3.txt,file1.json,file2.json}               
mkdir folder_1 folder_2 folder_3               
ls -la                 
mv {file1.txt,file1.json} folder_1                   
EOF  
```           
            
* Enter            
           
* chmod +x script.sh           
* ./script.sh               


