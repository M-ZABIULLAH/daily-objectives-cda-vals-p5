# Jour 48 - Lundi 05 Mai 2025

## Objectifs du jour

### Programmation Orientée Objet - Introduction et manipulation de base

- [ ] Découverte des types de programmation possibles (avantages et inconvénients de chacun)
  - [ ] Impérative
  - [ ] Procédurale
  - [ ] Orientée objet
  - [ ] Fonctionnelle
- [ ] Découverte des concepts clés de la POO :
  - [ ] Classe
  - [ ] Objet
  - [ ] Attribut
  - [ ] Méthode
  - [ ] Instanciation
  - [ ] Constructeur
  - [ ] Accesseurs
  - [ ] Encapsulation





```
```


#  برنامه‌نویسی شی‌گرا (POO) – مقدمه و مفاهیم پایه

##  بخش اول: آشنایی با انواع سبک‌های برنامه‌نویسی

###  1. برنامه‌نویسی امری (Impérative)
-  تعریف: برنامه‌نویس به سیستم دستور می‌دهد چه کارهایی را به ترتیب انجام دهد.
-  مزایا:
  - کنترل دقیق روی روند اجرا
  - مناسب برای الگوریتم‌های ساده
-  معایب:
  - پیچیده و سخت نگهداری در پروژه‌های بزرگ
  - تکرار زیاد کد

---

###  2. برنامه‌نویسی رویه‌ای (Procédurale)
-  تعریف: برنامه به مجموعه‌ای از توابع (procedure/function) تقسیم می‌شود.
-  مزایا:
  - سازمان‌دهی بهتر نسبت به سبک امری
  - آسان‌تر برای تست و اشکال‌زدایی
-  معایب:
  - هنوز قابلیت بازاستفاده و توسعه‌پذیری محدود است
  - مشکل در مدیریت داده‌ها در پروژه‌های بزرگ

---

###  3. برنامه‌نویسی شی‌گرا (Orientée Objet)
-  تعریف: همه چیز در قالب اشیاء (objects) و کلاس‌ها تعریف می‌شود.
-  مزایا:
  - قابلیت توسعه‌پذیری و نگهداری بالا
  - کپسوله‌سازی، وراثت و چندریختی
-  معایب:
  - یادگیری اولیه دشوارتر
  - پیچیدگی در پروژه‌های ساده

---

###  4. برنامه‌نویسی تابعی (Fonctionnelle)
-  تعریف: بر پایه توابع ریاضی و بدون حالت (stateless) طراحی می‌شود.
-  مزایا:
  - کدهای کوچک‌تر، خواناتر
  - جلوگیری از عوارض جانبی (side-effects)
-  معایب:
  - سخت‌تر برای درک و پیاده‌سازی در برخی زبان‌ها
  - عملکرد پایین‌تر نسبت به دیگر روش‌ها در برخی موارد

---

##  بخش دوم: مفاهیم کلیدی در برنامه‌نویسی شی‌گرا (POO)

###  1. کلاس (Classe)
> قالب یا طرح اولیه برای ساخت اشیاء. شامل تعریف ویژگی‌ها (attributes) و رفتارها (methods).

```java
public class Personne {
    String nom;
    int age;
}
````

---

###  2. شیء (Objet)

> نمونه‌ای از یک کلاس. اشیاء حافظه واقعی می‌گیرند و قابل استفاده‌اند.

```java
Personne p1 = new Personne();
```

---

###  3. ویژگی (Attribut)

> متغیرهایی که وضعیت یک شیء را توصیف می‌کنند.

```java
p1.nom = "Zabiullah";
p1.age = 25;
```

---

###  4. متد (Méthode)

> عملکردهایی که شیء می‌تواند انجام دهد.

```java
public void afficherNom() {
    System.out.println("Nom: " + nom);
}
```

---

###  5. نمونه‌سازی (Instanciation)

> فرایند ساخت یک شیء از یک کلاس با استفاده از کلمه‌کلیدی `new`.

```java
Personne p2 = new Personne();
```

---

###  6. سازنده (Constructeur)

> متدی ویژه برای مقداردهی اولیه به یک شیء در زمان ساخت آن.

```java
public Personne(String nomInitial, int ageInitial) {
    nom = nomInitial;
    age = ageInitial;
}
```

---

###  7. دسترسی‌دهنده‌ها (Accesseurs)

> متدهایی مانند `get` و `set` برای دسترسی به ویژگی‌های شیء به صورت کنترل‌شده.

```java
public String getNom() {
    return nom;
}
public void setNom(String nouveauNom) {
    this.nom = nouveauNom;
}
```

---

###  8. کپسوله‌سازی (Encapsulation)

> پنهان‌سازی داده‌ها از دنیای بیرون با استفاده از `private` و فراهم‌کردن دسترسی امن از طریق `getter/setter`.

```java
private int age;

public int getAge() {
    return age;
}
public void setAge(int age) {
    if (age > 0) {
        this.age = age;
    }
}
```

---


#  مفهوم کلاس و شیء در جاوا - همراه با پروژه‌ی کوچک

##  سناریو:
می‌خواهیم یک برنامه ساده برای **مدیریت اطلاعات دانش‌آموز** طراحی کنیم. در این برنامه، اطلاعاتی مانند نام، سن، و شماره کلاس دانش‌آموز نگهداری می‌شود.

---

##  مرحله 1: تعریف کلاس `Etudiant`

```java
// Etudiant.java
public class Etudiant {
    // Attributs
    String nom;
    int age;
    String classe;

    // Méthode pour afficher les informations
    public void afficherInfos() {
        System.out.println("Nom : " + nom);
        System.out.println("Âge : " + age);
        System.out.println("Classe : " + classe);
    }
}
````

---

##  مرحله 2: ایجاد شیء از کلاس در فایل اصلی برنامه

```java
// Main.java
public class Main {
    public static void main(String[] args) {
        // Instanciation d’un objet de type Etudiant
        Etudiant e1 = new Etudiant();

        // Affectation des valeurs
        e1.nom = "Zabiullah";
        e1.age = 25;
        e1.classe = "CDA - Promo 2025";

        // Appel de la méthode
        e1.afficherInfos();
    }
}
```

---

##  خروجی برنامه:

```
Nom : Zabiullah
Âge : 25
Classe : CDA - Promo 2025
```

---

##  نکات آموزشی:

| مفهوم             | توضیح                                             |
| ----------------- | ------------------------------------------------- |
| `Etudiant`        | یک کلاس است که ساختار دانش‌آموز را تعریف می‌کند.  |
| `e1`              | یک شیء (instance) از کلاس `Etudiant` است.         |
| `afficherInfos()` | یک متد است که اطلاعات شیء را در کنسول چاپ می‌کند. |

---

##  تمرین پیشنهادی:

 یک متد به نام `changerClasse(String nouvelleClasse)` به کلاس `Etudiant` اضافه کن تا بتوان کلاس دانش‌آموز را تغییر داد.

می‌خواهی این تمرین را هم با پاسخ بنویسم؟
