Сайн байна уу? 1234.mn -ны сургалтын тэмдэглэл /windows 10 pro os/

http://1234.mn/course/108


ВЭБ САЙТУУД
Хичээлд холбоотой вэб сайтууд
	https://github.com                                        - github бүртгэлийн сэрвэр
	https://git-scm.com/download/win                          - git татах
	https://cmder.net/                                        - линукс консол / Unicode дэмждэг
	https://misc.flogisoft.com/bash/tip_colors_and_formatting - bash өнгө болон форматын тайлбар
	http://bashrcgenerator.com/                               - bash rc үүсгэгч
	https://desktop.github.com/                               - Git Desktop хувилбар татах
	https://sourcetreeapp.com/                                - Branch мод хэлбэрээр хардаг програм / Git үйлдэлүүд хийх боломжтой
	https://github.com/git1234mn/commands                     - 1234.mn Сургалтын github


================================= GIT CONFIG ========================================================================
Git тохиргооны файл хаана байдаг вэ
	C:\Program Files\Git\etc\profile.d\git-prompt.sh
Хэрэглэгчийн Git тохиргоо
	C:\Users\user1\.config\git\git-prompt.sh
  

================================ BASH COMMAND =========================================================================
Bash - Bourne Again SHell
echo $HOME     - 
echo $MSYSTEM
clear
cd Folder
cat fileName  - file харах
nano fileName - file editor


======================================== Git - Файлын амьдралын цикл / Файлын төлөв ======================================

UNTRACKED	  - Мөрдлөггүй / Бүртгэлгүй
            Дөнгөж шинээр үүссэн файлууд
MODIFIED 	  - Өөрчлөгдсөн

STAGED 		  - Сонгогдсон

UNMODIFIED	- Өөрчлөлтгүй
            Git бүртгэсэнээс хойш өөрчлөлт ороогүй

================================= GIT COMMAND ========================================================================
ҮНДСЭН КОМАНДУУД 
git clone https://github.com/userName/ProjectName -Клон хийх
  Нэр томъёо: fork - Вэб сайт дээрээс салаалах ба өөрийн github руу оруулж ирэх

git status  
            - Одоо юу өөрчөгдсөн харах
git log     
            - Өөрчлөлтийн түүхүүд

 
git remote -v      
            - Github холболт хийсэн эсэх шалгах
                -Хоосон бол холболт хийгдээгүй
                -Холболтой бол доорх шиг харагдана
                    origin  https://github.com/userName/projectName.git (fetch)
                    origin  https://github.com/userName/projectName.git (push)
                      -	origin - Эх үүсвэр
                      - fetch - Татаж авах - Хаягны хойно байвал
                      - push - Илгээх - Хаягны хойно байвал



git remote add origin "https://github.com/userName/projectName.git"
              - Шинэ холболт хийх
              - local user үүсгэх
	            - тухайн project дотороо очиж хийх
	            - 

rm -rf .git
           - //git устгах

//nemelt medeelel
git remote --help

======================== Git -тэй кодтой ажиллах Үндсэн командууд =====================

1.git init      | git үүсгэх
2.git status    | өөрчлөлт харах
3.git add       | STAGING-д Нэмэх
4.git commit    | өөрчлөлт хадгалах
5.git push      | server лүү илгээх
6.git pull      | serverees tataj awah
7.git checkout  | ali neg tuuhiin kodiig gargaj awah


git add .   
            - staging - буюу тээвэрлэх машинд оруулах
            Нэр томъёо: staging - түр зуурын бөөгнүүлэн байршуулах газар
      git add *
      git add .
      git add -A 
            - бүгдийн ADD хийх      
      git add file2.txt 
            - зөвхөн file2.txt файлыг ADD хийх
git -c user.email="githubmail@anymail.com" -c user.name="uername1" commit -m "commit1" 
            - комит хийх / Холболт хийгээгүй үед өөрийн майл хэрэглэгчийн нэр шаардагатай
          
git commit -m 'Энд ямар нэг тайлбар бичнэ үү'
            - комит хийх / Холболт хийгдсэн буюу логин хийгдсэн үед

git push origin master
            - server-н master лүү илгээх
git push
            - ?? засах хэрэгтэй
            - 
git checkout -- . 
            - Сэрвэрээс код авах

======================== Git -тэй кодтой ажиллах Бусад командууд =====================

//Stage ээс буцаах
git restore --staged file1.txt index.html
git reset head 1.txt
git rm --cached 2.txt

//file сэргээх буцаах
git restore index.html file1.txt
git checkout -- index.html 

================================= GIT CONFIG ========================================================================

git config -l   
            - Тохиргоо харах
            
git config -l --show-origin
            - Бүх тохиргоо байрлах замтай харах


// Global config
git config --global user.email "user1@mail.com"
            - Өөрийн мэйлийг оруулах
git config --global user.name "user1"
            - Өөрийн нэрийг оруулах
// Local config
git config --local user.email "user2@gmail.com"
            - Өөрийн мэйлийг оруулах
git config --local user.name "user2"
            - Өөрийн нэрийг оруулах


//merge файл засах editor харах
git config --list
git config --global core.editor

// editor солих
git config --global core.editor "nano"
            - nano болгох

================================= GIT Суулгах ========================================================================
git init
            - суулгах төсөл / project -н сан д очиж хийнэ








======================================== Commit ================================================================================

commit бүр давтагдахшгүй sha1 код той

//commit мод мэдээлэл харах боломжтой - эцэг/parent/ нь хэн бэ харах
git cat-file -p 3c8619440a1dd4af74eab40201ebc626fe9d8e4d

//git бүгдийн шууд комит хийх  АНХААР зөвхөн шинээр үүссэн файлууд байвал үйлчилэхгүй, харин холилдсон байвал болно
// Санамсаргүй үүсэн байж магадгүй тул сэргийл байгаа, Ядаж нэгийн бүртгээд эхлэсэн үед л болно
git commit -a -m "коммит мсж"

//Commit уудын аль нэгрүү үсрэж очих буюу тэр үед очих бол
git checkout hashcode
	Аль нэг хувилбар дээр ажиллах тул master- нь HEAD ээс өөр тул салсан мэдээлэл өгнө

// Буцаад мастер-head рүү очих
git checkout master


======================================== Branch ================================================================================

Эхлэхдээ MASTER branch үүсэх юм 
//branch ийг харах
git branch

//шинэ branch үүсгэх
git branch dev
git branch tester

//Байвал шилжих байхгүй бол үүсгэх
git checkout -b dev

//dev branch Хаана зааж байгааг харах
cat .git\refs\heads\dev

// branch дээр ажиллах буюу шилжих
git checkout dev

//Одоо head аль branch зааж байгааг харах
cat .git/head


// branch нэр солих
git branch -m dev dev123

// branch уудиыг харах
ls .git/refs/heads
git branch


// branch устгах -Өөрчлөлт нэгтгэл хийсэн эсэх сануулдаг
git branch -d tester

//branch хүчээр устгах
git branch -D tester



======================================== 2 branch merge - нэгтгэх ================================================================================

//merge хийх 2 арга байдаг.
	- git fast forward merge
		master дээр нэгч ажиллаагүй /өөрчлөлт/ бол хийхэд болно
		
	- код бүрээр шалгах арга /3 алхамт/

//хэнээс хэнрүү авах уу хүлээн авагчруу орж байгаад merge хийнэ
git merge login   
      - одоо байгаа branch руу login branch нэгтгэх

git commit 
      -Хэрэв зөрчилтэй бол Харилцах засах цонх гарч ирж болно. 
      -Хэрэв зөрчилгүй бол шууд хийгдэнэ
  
//merge болиулах
git merge --abort





