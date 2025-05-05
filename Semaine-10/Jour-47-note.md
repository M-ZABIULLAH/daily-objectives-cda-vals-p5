# Jour 47 - Vendredi 2 mai 2025

## Objectifs du jour

### Brief NetStream

- [x] Réalisation d'une grille d'évaluation
- [x] Correction croisée entre groupes

### Introduction à Java et à la POO

- [x] Découvrir l'environnement de développement Java
  - [x] Installation du JDK et configuration de l'IDE (Eclipse, IntelliJ, etc.)
  - [x] Premier programme "Hello World"
  - [x] Comprendre la compilation et l'exécution en Java
  - [x] Compiler et exécuter son premier programme sans IDE

- [ ] Découvrir la syntaxe basique
  - [ ] Réaliser une classe minimale
  - [ ] Utiliser la méthode d’entrée de l’application
  - [ ] Afficher des informations dans la console
  - [ ] Savoir récupérer des informations saisies au clavier
  - [ ] Utiliser les structures conditionnelles
  - [ ] Connaître les différentes structures répétitives

- [ ] Découvrir le mécanisme de typage 
  - [ ] Comprendre les types existants
  - [ ] Savoir convertir les variables d'un type à un autre

- [ ] Premiers pas en POO
  - [ ] Comprendre les concepts fondamentaux de la POO en Java
    - [ ] Classes et Objets
    - [ ] Attributs et Méthodes
    - [ ] Constructeurs
  - [ ] Définir une classe avec attributs
  - [ ] Créer une instance
  - [ ] Appeler une méthode d'instance

- [ ] Comprendre et corriger les erreurs
  - [ ] Lire un message de compilation
  - [ ] Stratégies de débogage de base

- [ ] Pour aller plus loin (optionnel)
  - [ ] Comprendre l'utilisation de Maven
  - [ ] Installer et configurer Maven sur son environnement
  - [ ] Savoir lire un fichier pom.xml
  - [ ] Créer un 1er projet Web à l'aide de SpringBoot

- [ ] Exercices pratiques
  - [ ] TP fourni
  - [ ] Exercice Devinette
  - [ ] Exercice Calculatrice



---
---
```
```

##  آشنایی با زبان Java و برنامه‌نویسی شی‌گرا (POO)

###  راه‌اندازی محیط توسعه Java

- **نصب JDK (Java Development Kit):**
  برای برنامه‌نویسی با جاوا، ابتدا باید JDK نصب شود که شامل ابزارهای موردنیاز برای کامپایل و اجرای برنامه‌های جاوا است.

- **انتخاب و پیکربندی IDE:**
  استفاده از محیط‌های توسعه مانند:
  - [x] Eclipse
  - [x] IntelliJ IDEA  
  برای نوشتن، اجرا و دیباگ راحت‌تر کدها.

- **اولین برنامه‌ی Hello World:**
  ```java
  public class HelloWorld {
      public static void main(String[] args) {
          System.out.println("سلام دنیا!");
      }
  }


این برنامه یک خروجی ساده در کنسول چاپ می‌کند.


###  کامپایل و اجرای برنامه جاوا

* **فرآیند کامپایل:**
  فایل `.java` با استفاده از دستور `javac` کامپایل می‌شود:

  ```bash
  javac HelloWorld.java
  ```

* **اجرای برنامه:**
  پس از کامپایل، فایل `.class` ایجاد شده و با دستور زیر اجرا می‌شود:

  ```bash
  java HelloWorld
  ```

* **اجرا در IDE:**
  با زدن دکمه "Run" در Eclipse یا IntelliJ برنامه اجرا می‌شود.

---

###  آشنایی با دستور زبان پایه جاوا

####  تعریف کلاس و متد اصلی

جاوا زبانی شی‌گراست، هر کد باید درون کلاس نوشته شود. متد اصلی برای شروع اجرای برنامه:

```java
public static void main(String[] args) {
    // کد اینجا اجرا می‌شود
}
```

####  چاپ در کنسول

برای نمایش پیام‌ها:

```java
System.out.println("متنی برای چاپ");
```

####  گرفتن ورودی از کاربر

برای دریافت ورودی از کاربر در کنسول:

```java
import java.util.Scanner;

Scanner input = new Scanner(System.in);
System.out.print("نام خود را وارد کنید: ");
String name = input.nextLine();
System.out.println("سلام " + name);
```

####  ساختارهای شرطی

```java
int age = 18;
if (age >= 18) {
    System.out.println("بزرگسال هستید");
} else {
    System.out.println("کم‌سن هستید");
}
```

#### حلقه‌ها

```java
for (int i = 0; i < 5; i++) {
    System.out.println("تکرار شماره: " + i);
}
```

---

###  سیستم نوع‌دهی (Typing) در جاوا

####  نوع‌های اولیه (Primitive types)

* `int` — عدد صحیح
* `double` — عدد اعشاری
* `char` — کاراکتر
* `boolean` — درست یا نادرست

#### تبدیل نوع (Casting)

```java
int x = 10;
double y = x; // تبدیل ضمنی

double a = 5.7;
int b = (int) a; // تبدیل صریح: نتیجه 5
```

---

##  گام‌های نخست در برنامه‌نویسی شی‌گرا (POO)

###  مفاهیم پایه:

* **کلاس (Class):** قالب ساخت اشیا
* **شیء (Object):** نمونه‌ای از یک کلاس
* **ویژگی (Attribute):** اطلاعات مربوط به شیء
* **متد (Method):** عملکردهایی که شیء می‌تواند انجام دهد
* **سازنده (Constructor):** متدی خاص که هنگام ساخت شیء فراخوانی می‌شود

###  تعریف کلاس با ویژگی و متد:

```java
public class Person {
    String name;
    int age;

    // سازنده
    public Person(String n, int a) {
        name = n;
        age = a;
    }

    // متد
    public void sayHello() {
        System.out.println("سلام! من " + name + " هستم.");
    }
}
```

###  ایجاد شیء و استفاده از متد:

```java
Person p1 = new Person("علی", 25);
p1.sayHello();
```

---

##  آشنایی با خطاها و دیباگ

###  خواندن پیام‌های کامپایل

پیام خطا به ما نشان می‌دهد:

* در کدام خط خطا وجود دارد
* نوع خطا (مثلاً syntax error، type mismatch و غیره)

###  استراتژی‌های دیباگ ساده:

* چاپ مقدار متغیرها با `System.out.println`
* بررسی مرحله به مرحله‌ی اجرای کد
* استفاده از ابزارهای دیباگ IDE

---

##  بخش پیشرفته (اختیاری)

###  آشنایی با Maven

* **Maven** یک ابزار مدیریت پروژه و وابستگی‌هاست.
* فایل پیکربندی: `pom.xml`
* نصب با استفاده از وب‌سایت رسمی یا با استفاده از package manager

###  ایجاد پروژه وب با Spring Boot

* استفاده از [https://start.spring.io/](https://start.spring.io/) برای تولید پروژه اولیه
* اجرای پروژه با `mvn spring-boot:run`

---

##  تمرینات عملی

###  تمرین: بازی حدس عدد

برنامه‌ای که یک عدد تصادفی انتخاب می‌کند و کاربر باید آن را حدس بزند.

###  تمرین: ماشین حساب ساده

برنامه‌ای که دو عدد گرفته و عملیات (+، -، \*، /) را انجام می‌دهد.

#  Comprendre la compilation et l'exécution en Java
##  درک کامپایل و اجرای برنامه در Java

زبان Java یک زبان **کامپایل‌شونده و اجراشونده روی ماشین مجازی (JVM)** است. فرآیند اجرا در دو مرحله انجام می‌شود:

1.  **کامپایل (Compilation)**  
   - با استفاده از دستور `javac`، کد منبع جاوا (مثلاً `Main.java`) به **bytecode** ترجمه می‌شود.  
   - خروجی این مرحله فایلی با پسوند `.class` است که توسط JVM قابل فهم است.

2.  **اجرا (Execution)**  
   - با استفاده از دستور `java`، فایل bytecode توسط JVM اجرا می‌شود.

---

##  Compiler et exécuter son premier programme sans IDE  
###  کامپایل و اجرای اولین برنامه بدون استفاده از IDE

###  مرحله 1: ایجاد فایل جاوا

```bash
nano Main.java
````

و سپس کد زیر را وارد کن:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Bonjour le monde !");
    }
}
```

ذخیره و خروج:

* `Ctrl + X`
* سپس `Y`
* و Enter

---

###  مرحله 2: کامپایل فایل جاوا

```bash
javac Main.java
```

در صورت موفقیت، فایل `Main.class` در همان مسیر ایجاد می‌شود.

---

###  مرحله 3: اجرای برنامه

```bash
java Main
```

 **خروجی برنامه:**

```
Bonjour le monde !
```

---

##  نکات مهم

* نام فایل (`Main.java`) باید دقیقاً با نام کلاس (`Main`) هم‌نام باشد.
* برای اجرای موفق، JDK باید به درستی نصب شده باشد و دستورات `javac` و `java` در مسیر سیستم (PATH) قرار داشته باشند.
* برای بررسی نسخه JDK نصب‌شده:

```bash
java -version
javac -version
```

* در صورت مشاهده خطای `command not found: javac`، JDK یا نصب نشده یا به درستی در محیط سیستم تنظیم نشده است.

---
```
```


#  Découvrir la syntaxe basique en Java  
##  آشنایی با سینتکس پایه در زبان Java

---

##  Réaliser une classe minimale  
###  ساختار پایه یک کلاس جاوا

در جاوا، همه‌چیز در قالب کلاس نوشته می‌شود. ساده‌ترین کلاس ممکن می‌تواند به این شکل باشد:

```java
public class Main {
    public static void main(String[] args) {
        // نقطه ورود به برنامه
    }
}
````

**توضیحات:**

* `public class Main`: تعریف یک کلاس عمومی به نام `Main`.
* `public static void main(String[] args)`: متد اصلی که هنگام اجرای برنامه فراخوانی می‌شود.

---

##  Utiliser la méthode d’entrée de l’application

###  استفاده از متد `main` به عنوان نقطه ورود

متد `main` مهم‌ترین متد در برنامه جاوا است. این متد باید دقیقاً با امضای زیر تعریف شود:

```java
public static void main(String[] args) {
    // کد برنامه در اینجا نوشته می‌شود
}
```

* `public`: قابل دسترسی عمومی
* `static`: بدون نیاز به ساخت شی
* `void`: بدون خروجی
* `String[] args`: آرایه‌ای از رشته‌ها که آرگومان‌های خط فرمان را نگه می‌دارد

---

##  Afficher des informations dans la console

###  نمایش متن در خروجی (کنسول)

برای نمایش پیام یا اطلاعات در کنسول از دستور `System.out.println` استفاده می‌شود:

```java
System.out.println("Bonjour !");
```

**خروجی:**

```
Bonjour !
```

---

## Savoir récupérer des informations saisies au clavier

###  دریافت ورودی از کاربر با استفاده از Scanner

برای گرفتن ورودی از کاربر از کلاس `Scanner` استفاده می‌کنیم:

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        System.out.print("Entrez votre nom: ");
        String nom = input.nextLine();

        System.out.println("Bonjour " + nom + " !");
    }
}
```

 **ورودی:**

```
Entrez votre nom: Alice
```

 **خروجی:**

```
Bonjour Alice !
```

---

##  Utiliser les structures conditionnelles

###  استفاده از ساختارهای شرطی (if, else if, else)

ساختار شرطی به شکل زیر است:

```java
int age = 20;

if (age < 18) {
    System.out.println("Mineur");
} else if (age == 18) {
    System.out.println("Exactement 18 ans");
} else {
    System.out.println("Majeur");
}
```

---

##  Connaître les différentes structures répétitives

###  حلقه‌ها در جاوا

###  Boucle `while`

```java
int i = 0;
while (i < 5) {
    System.out.println(i);
    i++;
}
```
###  Boucle `for`

```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

###  Boucle `do...while`

```java
int i = 0;
do {
    System.out.println(i);
    i++;
} while (i < 5);
```

---

```
```
---

#  Découvrir le mécanisme de typage
##  آشنایی با سیستم نوع‌دهی (Typage) در Java

جاوا یک زبان **ایستا (statiquement typé)** و **قوی (fortement typé)** است؛ یعنی:
- هر متغیر **باید نوع مشخصی داشته باشد**.
- تبدیل نوع‌ها (type casting) باید **صراحتاً یا طبق قواعد خاصی** انجام شود.

---

##  Comprendre les types existants
###  انواع داده‌ها در جاوا

جاوا دارای دو دسته اصلی نوع داده است:

### 🔹 Types primitifs (اولیه)

| Type      | Taille | Exemple     |
|-----------|--------|-------------|
| `int`     | 4 bytes| `int age = 25;` |
| `double`  | 8 bytes| `double pi = 3.14;` |
| `float`   | 4 bytes| `float f = 2.5f;` |
| `char`    | 2 bytes| `char c = 'A';` |
| `boolean` | 1 bit  | `boolean b = true;` |
| `long`    | 8 bytes| `long l = 123456789L;` |
| `short`   | 2 bytes| `short s = 1000;` |
| `byte`    | 1 byte | `byte b = 100;` |

###  Types objets (référencés)
- `String`, `Scanner`, `List`, `ArrayList`, `Date`, ...
```java
String nom = "Alice";
````

---

##  Savoir convertir les variables d'un type à un autre

###  تبدیل نوع‌ها (Type Conversion)

###  Casting implicite (automatique)

وقتی از نوع کوچکتر به بزرگتر تبدیل کنیم:

```java
int i = 10;
double d = i;  // OK
```

###  Casting explicite (دستی)

وقتی از نوع بزرگتر به کوچکتر تبدیل کنیم:

```java
double d = 10.5;
int i = (int) d; // 10
```

###  تبدیل رشته به عدد

```java
String nombre = "123";
int x = Integer.parseInt(nombre);
double y = Double.parseDouble("3.14");
```

###  تبدیل عدد به رشته

```java
int n = 42;
String texte = String.valueOf(n); // "42"
```

---

##  مثال کامل برای تمرین

```java
import java.util.Scanner;

public class TypeDemo {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Entrez un nombre entier: ");
        String texte = input.nextLine();

        int valeur = Integer.parseInt(texte);

        double resultat = valeur / 2.0;

        System.out.println("Résultat: " + resultat);
    }
}
```

 **ورودی:** `15`
 **خروجی:** `Résultat: 7.5`

---


#  Premiers pas en POO en Java
##  گام‌های اولیه در برنامه‌نویسی شی‌گرا (POO) با زبان جاوا

---

##  Comprendre les concepts fondamentaux de la POO
###  درک مفاهیم پایه برنامه‌نویسی شی‌گرا

مفاهیم اصلی در POO شامل موارد زیر هستند:
- **Classe (کلاس)**: قالب یا مدل یک شی
- **Objet (شی)**: نمونه‌ای از کلاس
- **Attribut (ویژگی / متغیر)**: داده‌هایی که شی نگهداری می‌کند
- **Méthode (متد / تابع)**: عملیاتی که روی داده‌ها انجام می‌شود
- **Constructeur**: تابع خاص برای ساخت یک شی جدید

---

##  Classes et Objets
###  تعریف کلاس و ایجاد شی (Object)

```java
public class Personne {
    // Attributs
    String nom;
    int age;

    // Méthode
    void saluer() {
        System.out.println("Bonjour, je m'appelle " + nom + ".");
    }
}
````

###  ایجاد یک شی و استفاده از آن:

```java
public class Main {
    public static void main(String[] args) {
        Personne p = new Personne();
        p.nom = "Alice";
        p.age = 25;
        p.saluer();  // Bonjour, je m'appelle Alice.
    }
}
```

---

##  Constructeurs

###  سازنده‌ها (Constructors)

سازنده متدی است که هنگام ساخت شی صدا زده می‌شود:

```java
public class Personne {
    String nom;
    int age;

    // Constructeur
    Personne(String n, int a) {
        nom = n;
        age = a;
    }

    void afficher() {
        System.out.println(nom + " a " + age + " ans.");
    }
}
```

```java
public class Main {
    public static void main(String[] args) {
        Personne p1 = new Personne("Bob", 30);
        p1.afficher();  // Bob a 30 ans.
    }
}
```

---

##  Appeler une méthode d'instance

###  فراخوانی متد یک شی

متدهای کلاس از طریق اشیاء آن کلاس فراخوانی می‌شوند:

```java
CompteBancaire compte = new CompteBancaire("Jean", 1000);
compte.afficherSolde();
```

---

##  Comprendre et corriger les erreurs

###  درک و اصلاح خطاها

### 🔹 Lire un message de compilation

مثال خطا:

```java
System.oot.println("Salut");
```

 **خطا:**

```
error: cannot find symbol
System.oot.println("Salut");
       ^
```

 راه‌حل: اصلاح `oot` به `out`

---

## Stratégies de débogage de base

###  تکنیک‌های اولیه رفع خطا

* خواندن دقیق پیغام خطا
* بررسی املا متغیرها و نام کلاس‌ها
* استفاده از `System.out.println()` برای نمایش مقادیر و موقعیت‌ها
* تست بخش‌به‌بخش کد

---

##  تمرین پیشنهادی

```java
public class Livre {
    String titre;
    String auteur;

    Livre(String t, String a) {
        titre = t;
        auteur = a;
    }

    void afficherInfo() {
        System.out.println("Titre: " + titre + ", Auteur: " + auteur);
    }
}

public class Main {
    public static void main(String[] args) {
        Livre livre1 = new Livre("Le Petit Prince", "Saint-Exupéry");
        livre1.afficherInfo();
    }
}
```

 **خروجی:**

```
Titre: Le Petit Prince, Auteur: Saint-Exupéry
```

---


#  Pour aller plus loin : Maven et Spring Boot

##  Maven چیست؟
**Maven** یک ابزار مدیریت پروژه و ساخت (build) برای پروژه‌های Java است.  
امکانات آن شامل:
- مدیریت وابستگی‌ها (dependencies)
- ساخت خودکار (compilation, test, packaging)
- ساختاردهی استاندارد به پروژه‌ها

---

##  Installer et configurer Maven sur son environnement
###  نصب و پیکربندی Maven در لینوکس

```bash
sudo apt update
sudo apt install maven
mvn -v   # بررسی نصب
````

###  ساختار پیش‌فرض پروژه Maven

```
mon-projet/
├── pom.xml
└── src/
    ├── main/
    │   ├── java/
    │   └── resources/
    └── test/
```

---

##  Savoir lire un fichier `pom.xml`

فایل `pom.xml` قلب پروژه Maven است.

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" ...>
  <modelVersion>4.0.0</modelVersion>

  <groupId>com.exemple</groupId>
  <artifactId>demo</artifactId>
  <version>1.0-SNAPSHOT</version>

  <dependencies>
    <!-- Dépendance Spring Boot -->
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-web</artifactId>
      <version>3.1.0</version>
    </dependency>
  </dependencies>
</project>
```

---

## Créer un 1er projet Web avec Spring Boot

###  ساخت پروژه Spring Boot با استفاده از Spring Initializr:

1. برو به: [https://start.spring.io](https://start.spring.io)
2. مشخصات را وارد کن:

   * Project: Maven
   * Language: Java
   * Packaging: Jar
   * Dependencies: Spring Web
3. روی **Generate** کلیک کن و فایل ZIP را دانلود کن.
4. پروژه را در IntelliJ یا Eclipse باز کن.

---

##  مثال ساده – API ساده با Spring Boot

### 🔹 `DemoApplication.java`

```java
@SpringBootApplication
public class DemoApplication {
    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }
}
```

### 🔹 `HelloController.java`

```java
@RestController
public class HelloController {

    @GetMapping("/hello")
    public String saluer() {
        return "Bonjour depuis Spring Boot!";
    }
}
```

 با اجرای برنامه و رفتن به آدرس `http://localhost:8080/hello` در مرورگر، خروجی زیر را می‌بینی:

```
Bonjour depuis Spring Boot!
```

---

##  Exercices pratiques

###  TP fourni

* بررسی پروژه نمونه
* اجرای دستورات `mvn clean install` و `mvn spring-boot:run`

###  Exercice Devinette

* ساخت برنامه‌ای برای حدس عدد با استفاده از کلاس و Scanner

###  Exercice Calculatrice

* طراحی یک کلاس `Calculatrice` با متدهایی مثل `addition`, `soustraction`, `multiplication`, `division`
* استفاده از `Scanner` برای دریافت ورودی کاربر

---


#  تمرین: بازی حدس عدد (Jeu de Devinette)

##  هدف:
برنامه‌ای بنویس که:
- عددی تصادفی بین 1 تا 100 انتخاب کند.
- کاربر تلاش کند آن را حدس بزند.
- به کاربر بگوید که عدد واردشده بزرگ‌تر یا کوچک‌تر از عدد واقعی است.
- تعداد تلاش‌ها را بشمارد.

---

##  اجزای مورد نیاز:
- استفاده از `Scanner` برای دریافت ورودی کاربر
- استفاده از `Random` برای تولید عدد تصادفی
- استفاده از حلقه `while`
- استفاده از شرط `if...else`

---

##  کد کامل به زبان جاوا:

```java
import java.util.Scanner;
import java.util.Random;

public class Devinette {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        int nombreSecret = random.nextInt(100) + 1; // عدد بین 1 تا 100
        int tentative;
        int compteur = 0;

        System.out.println("🎮 Bienvenue au jeu de devinette !");
        System.out.println("Devinez un nombre entre 1 et 100 :");

        do {
            System.out.print("Votre proposition : ");
            tentative = scanner.nextInt();
            compteur++;

            if (tentative < nombreSecret) {
                System.out.println(" Trop petit !");
            } else if (tentative > nombreSecret) {
                System.out.println(" Trop grand !");
            } else {
                System.out.println(" Bravo ! Vous avez trouvé en " + compteur + " tentatives.");
            }

        } while (tentative != nombreSecret);

        scanner.close();
    }
}
````

---

##  خروجی نمونه:

```
 Bienvenue au jeu de devinette !
Devinez un nombre entre 1 et 100 :
Votre proposition : 50
 Trop petit !
Votre proposition : 75
 Trop grand !
Votre proposition : 63
 Bravo ! Vous avez trouvé en 3 tentatives.
```

---

## مفاهیم پوشش داده‌شده:

* متغیرها و ورودی از کاربر
* تولید عدد تصادفی
* شرط‌ها (if-else)
* حلقه تکرار (do-while)
* شمارش تعداد تلاش‌ها

---


#  تمرین: ساخت ماشین‌حساب ساده در Java

##  هدف:
ساخت یک برنامه کنسولی در جاوا که:
- عملیات ریاضی ساده مانند جمع، تفریق، ضرب و تقسیم را انجام دهد.
- با استفاده از کلاس `Scanner` ورودی اعداد و عملگر را از کاربر بگیرد.
- نتیجه را نمایش دهد.

---

##  اجزای مورد نیاز:
- استفاده از `Scanner` برای دریافت ورودی
- استفاده از `if`, `switch` یا `else if` برای انتخاب عملیات
- استفاده از `double` برای پشتیبانی از اعداد اعشاری

---

##  کد کامل به زبان جاوا:

```java
import java.util.Scanner;

public class Calculatrice {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println(" Bienvenue dans la calculatrice Java !");
        
        System.out.print("Entrez le premier nombre : ");
        double nombre1 = scanner.nextDouble();

        System.out.print("Entrez l'opérateur (+, -, *, /) : ");
        char operateur = scanner.next().charAt(0);

        System.out.print("Entrez le deuxième nombre : ");
        double nombre2 = scanner.nextDouble();

        double resultat;

        switch (operateur) {
            case '+':
                resultat = nombre1 + nombre2;
                System.out.println("Résultat = " + resultat);
                break;
            case '-':
                resultat = nombre1 - nombre2;
                System.out.println("Résultat = " + resultat);
                break;
            case '*':
                resultat = nombre1 * nombre2;
                System.out.println("Résultat = " + resultat);
                break;
            case '/':
                if (nombre2 != 0) {
                    resultat = nombre1 / nombre2;
                    System.out.println("Résultat = " + resultat);
                } else {
                    System.out.println(" Erreur : Division par zéro !");
                }
                break;
            default:
                System.out.println(" Opérateur non valide.");
        }

        scanner.close();
    }
}
````

---

## خروجی نمونه:

```
Bienvenue dans la calculatrice Java !
Entrez le premier nombre : 10
Entrez l'opérateur (+, -, *, /) : *
Entrez le deuxième nombre : 5
Résultat = 50.0
```

---

## مفاهیم پوشش داده‌شده:

* متغیرها (double, char)
* دریافت ورودی با Scanner
* شرط و انتخاب عملیات با switch-case
* بررسی خطای تقسیم بر صفر

---
