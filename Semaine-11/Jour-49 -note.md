# Jour 49 - Mardi 06 Mai 2025

## Objectifs du jour

### Programmation Orientée Objet - Abstraction et Collections

- [ ] Découverte de l'Abstraction
  - [ ] Bilan sur l'héritage
  - [ ] Notion de classes abstraites
  - [ ] Notion d'interface

- [ ] Découvrir les Collections Java
  - [ ] List (ArrayList, LinkedList)
  - [ ] Set (HashSet, TreeSet)
  - [ ] Map (HashMap, TreeMap)
  - [ ] Utilisation des Generics

- [ ] Initiation aux bonnes pratiques
  - [ ] Découverte du principe SOLID

- [ ] Exercices pratiques
  - [ ] Manipuler une liste d'objets (ajouter, supprimer, trier)





---

```
```




###  Programmation Orientée Objet - Abstraction et Collections

---

####  Découverte de l'Abstraction

- **Bilan sur l'héritage**  
  🔸 Revoir les concepts de l'héritage en Java : superclasses, sous-classes, override, etc.

- [ ] **Notion de classes abstraites**  
  🔸 Comprendre la déclaration d’une classe abstraite avec `abstract`.  
  🔸 Savoir quand utiliser une classe abstraite pour factoriser du comportement commun.

- [ ] **Notion d'interface**  
  🔸 Différence entre une interface et une classe abstraite.  
  🔸 Savoir implémenter une interface avec `implements`.

---

#### 🔸 Découvrir les Collections Java

- [ ] **List (ArrayList, LinkedList)**  
  🔸 Comprendre les différences entre les deux.  
  🔸 Ajouter, accéder et supprimer des éléments.

- [ ] **Set (HashSet, TreeSet)**  
  🔸 Notion d'unicité des éléments.  
  🔸 Tri automatique avec `TreeSet`.

- [ ] **Map (HashMap, TreeMap)**  
  🔸 Association clé/valeur.  
  🔸 Accès rapide avec les clés.  
  🔸 Tri des clés dans `TreeMap`.

- [ ] **Utilisation des Generics**  
  🔸 Définir des collections typées pour éviter les erreurs d’exécution.  
  🔸 Syntaxe : `ArrayList<String>`, `HashMap<Integer, String>`, etc.

---

#### ✅ Initiation aux bonnes pratiques

- [ ] **Découverte du principe SOLID**  
  🔸 Introduction aux cinq principes SOLID :  
    - **S**: Single Responsibility  
    - **O**: Open/Closed  
    - **L**: Liskov Substitution  
    - **I**: Interface Segregation  
    - **D**: Dependency Inversion

---

#### 🛠️ Exercices pratiques

- [ ] **Manipuler une liste d'objets**  
  🔸 Créer une `ArrayList` d’objets personnalisés (ex : Étudiant, Livre...)  
  🔸 Ajouter des éléments  
  🔸 Supprimer certains éléments  
  🔸 Trier la liste selon un critère (nom, ID, etc.)
```
```

---


###  مفهوم کلاس‌های انتزاعی در جاوا (Abstract Classes)

####  تعریف:
کلاس‌های انتزاعی در جاوا با کلیدواژه `abstract` تعریف می‌شوند و نمی‌توان از آن‌ها مستقیماً شیء (object) ساخت. این کلاس‌ها معمولاً شامل متدهایی هستند که پیاده‌سازی ندارند و باید در کلاس‌های فرزند (زیرکلاس‌ها) پیاده‌سازی شوند.

#### ساختار پایه:

```java
abstract class Animal {
    String nom;

    public Animal(String nom) {
        this.nom = nom;
    }

    // متد انتزاعی: بدون پیاده‌سازی
    abstract void crier();

    // متد معمولی
    void dormir() {
        System.out.println(nom + " خوابیده است...");
    }
}
````

####  زیرکلاس نمونه:

```java
class Chien extends Animal {
    public Chien(String nom) {
        super(nom);
    }

    @Override
    void crier() {
        System.out.println(nom + " پارس می‌کند!");
    }
}
```

#### ▶ استفاده از کلاس:

```java
public class Main {
    public static void main(String[] args) {
        Chien rex = new Chien("رِکس");
        rex.crier();   // رِکس پارس می‌کند!
        rex.dormir();  // رِکس خوابیده است...
    }
}
```

---

###  تمرین پیشنهادی:

** تمرین 1:**

یک کلاس انتزاعی به نام `Vehicule` ایجاد کن که شامل موارد زیر باشد:

* یک فیلد `marque` برای برند وسیله نقلیه
* یک متد معمولی `afficherInfos()` برای نمایش اطلاعات برند
* یک متد انتزاعی `demarrer()` برای راه‌اندازی وسیله نقلیه

سپس دو کلاس `Voiture` (ماشین) و `Moto` (موتورسیکلت) ایجاد کن که از `Vehicule` ارث‌بری کنند و متد `demarrer()` را پیاده‌سازی نمایند.

```

---

اگر خواستی بخش بعدی یعنی **interface** را هم به همین شکل ادامه بدهم، فقط بگو «ادامه بده».
```


---

###  Notion de classes abstraites

#### تعریف:

کلاس‌های انتزاعی (abstract) کلاس‌هایی هستند که نمی‌توان از آن‌ها مستقیماً شیء ساخت. آن‌ها برای مشخص کردن ساختار پایه‌ای طراحی شده‌اند که کلاس‌های فرزند باید آن را پیاده‌سازی کنند.
####  ساختار عمومی:

```java
abstract class Animal {
    String nom;

    public Animal(String nom) {
        this.nom = nom;
    }

    // méthode abstraite (sans implémentation)
    abstract void crier();

    // méthode normale
    void dormir() {
        System.out.println(nom + " dort...");
    }
}
```

کلاس فرزند:

```java
class Chien extends Animal {
    public Chien(String nom) {
        super(nom);
    }

    @Override
    void crier() {
        System.out.println(nom + " aboie !");
    }
}
```

استفاده:

```java
public class Main {
    public static void main(String[] args) {
        Chien rex = new Chien("Rex");
        rex.crier();   // Rex aboie !
        rex.dormir();  // Rex dort...
    }
}
```

---

###  تمرین پیشنهادی:

** تمرین 1:**
یک کلاس انتزاعی به نام `Vehicule` بساز که دارای:

* یک فیلد `marque`
* یک متد `afficherInfos()` برای نمایش مارک خودرو
* یک متد انتزاعی `demarrer()`

سپس دو کلاس `Voiture` و `Moto` بساز که از `Vehicule` ارث‌بری کنند و متد `demarrer()` را پیاده‌سازی نمایند.

---
```
```

---

#  برنامه‌نویسی شی‌گرا: انتزاع و مجموعه‌ها در جاوا (Abstraction et Collections)

## 1. آشنایی با انتزاع (Abstraction)

###  بررسی ارث‌بری (Bilan sur l'héritage)
ارث‌بری یکی از اصول پایه برنامه‌نویسی شی‌گراست که به یک کلاس اجازه می‌دهد خصوصیات (attributes) و رفتارها (methods) کلاس دیگر را به ارث ببرد.
- کلاس والد: کلاس پایه‌ای که سایر کلاس‌ها از آن ارث می‌برند.
- کلاس فرزند: کلاسی که از کلاس والد ویژگی‌ها و متدها را به ارث می‌برد.

 مزایا:
- کاهش کد تکراری
- افزایش قابلیت استفاده مجدد

---

###  مفهوم کلاس‌های انتزاعی (Notion de classes abstraites)
کلاس‌های انتزاعی با کلیدواژه `abstract` تعریف می‌شوند و نمی‌توان از آن‌ها شیء ساخت. این کلاس‌ها برای تعریف ساختار کلی استفاده می‌شوند.
- می‌توانند هم متد پیاده‌سازی‌شده و هم متد بدون پیاده‌سازی داشته باشند.
- زیرکلاس‌ها باید متدهای انتزاعی را پیاده‌سازی کنند.

 کاربرد: طراحی چارچوبی که پیاده‌سازی‌اش به کلاس‌های فرزند سپرده می‌شود.

---

###  مفهوم اینترفیس (Notion d’interface)
یک Interface مانند قراردادی است که کلاس‌ها موظف به اجرای آن هستند.
- فقط شامل امضای متدهاست (تا Java 8).
- کلاس‌هایی که `implements` می‌کنند باید تمام متدها را پیاده‌سازی کنند.
- یک کلاس می‌تواند چندین اینترفیس را پیاده‌سازی کند (برخلاف ارث‌بری که فقط یک کلاس پایه ممکن است).

 تفاوت با کلاس انتزاعی:
- Interface فقط شامل متدهای انتزاعی است (پیش از Java 8).
- یک کلاس می‌تواند از یک کلاس انتزاعی ارث ببرد ولی چند اینترفیس را پیاده‌سازی کند.

---

## 2.  آشنایی با مجموعه‌ها در جاوا (Collections Java)

###  لیست‌ها (List)
ساختار داده‌ای که عناصر را به ترتیب نگه می‌دارد و امکان تکرار داده‌ها را فراهم می‌کند.

- **ArrayList**: لیستی با دسترسی سریع‌تر، اما کندتر در اضافه‌کردن وسط لیست.
- **LinkedList**: مناسب برای درج/حذف سریع در ابتدا/میانه، ولی دسترسی کندتر.

---

###  مجموعه‌ها (Set)
ساختاری که داده‌های تکراری را نمی‌پذیرد.

- **HashSet**: بدون ترتیب خاص، سریع‌تر برای عملیات پایه.
- **TreeSet**: عناصر را مرتب نگه می‌دارد (بر اساس ترتیب طبیعی یا تعریف‌شده).

---

###  نگاشت‌ها (Map)
کلید و مقدار (key-value) را ذخیره می‌کند.

- **HashMap**: سریع و بدون ترتیب.
- **TreeMap**: مرتب‌شده بر اساس کلیدها.

---

###  استفاده از Generics
با استفاده از Generics می‌توان تایپ داده‌ها را هنگام تعریف مجموعه مشخص کرد تا امنیت نوعی (type safety) افزایش یابد.
مثال:
```java
List<String> noms = new ArrayList<>();
Map<Integer, String> utilisateurs = new HashMap<>();
````

---

## 3.  مقدمه‌ای بر اصول طراحی خوب (Bonnes pratiques)

###  آشنایی با اصول SOLID

اصول SOLID پنج اصل کلیدی برای طراحی کلاس‌های قابل توسعه و نگهداری هستند:

1. **S** - Single Responsibility Principle (اصل تک‌وظیفگی)

   * هر کلاس فقط یک مسئولیت داشته باشد.
2. **O** - Open/Closed Principle (باز برای توسعه، بسته برای تغییر)

   * کد باید قابل توسعه باشد بدون نیاز به تغییر کلاس‌های موجود.
3. **L** - Liskov Substitution Principle (اصل جانشینی لیسکوف)

   * اشیای کلاس‌های فرزند باید قابل جایگزینی با والد خود باشند.
4. **I** - Interface Segregation Principle (تفکیک اینترفیس)

   * نباید کلاس‌ها را مجبور به پیاده‌سازی متدهایی کنیم که از آن‌ها استفاده نمی‌کنند.
5. **D** - Dependency Inversion Principle (وارونگی وابستگی)

   * وابستگی‌ها باید به سمت اینترفیس‌ها باشد، نه کلاس‌های پیاده‌سازی‌شده.

---
