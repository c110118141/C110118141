# Java程式碼都在這一個Markdown
---
### Q.請新增一個CShape的子類別CTriangle，其constructor 共有三個double的參數 a,b,c (為直角三角形的三個邊長)，其面積為0.5*a*b，請寫出CTriangle的類別程式與產生其物件的main 程式(顏色為紅色，a=3, b=4, c=5) 程式碼請放在個人的github 答案請列出其連結

#### CShape.java:
```java=
abstract class CShape{
  protected String color;

  public abstract void show();

  public void setColor(String input){
      color = input;
  }
}
```

#### CTriangle.java:
```java=
class CTriangle extends CShape{
  double a1,b1,c1;
  public CTriangle(double a,double b,double c){
    a1 = a;
    b1 = b;
    c1 = c;
  }
  public void show() {
    System.out.println("color is "+color);
    System.out.println("area is "+0.5*a1*b1);
  }
 
}
```

#### app.java:
```java=
 public class app {
   public static void main(String[] args) {
    CTriangle t = new CTriangle(3, 4, 5);
    t.setColor("red");
    t.show();
  }
}

```
---
### 一個學生上0-10門課(好難)
```java=
import java.util.ArrayList;
import java.util.List;

public class Student {
    private String name;
    private List<Course> courses;
    public Student(String name) {
        this.name = name;
        this.courses = new ArrayList<>();
    }
    public boolean addCourse(Course course) {
        if (courses.size() < 10) {
            courses.add(course);
            return true;
        }
        return false;
    }
    public boolean removeCourse(Course course) {
        return courses.remove(course);
    }
    public List<Course> getCourses() {
        return courses;
    }
}

public class Course {
    private String courseName;
    public Course(String courseName) {
        this.courseName = courseName;
    }
}
```
