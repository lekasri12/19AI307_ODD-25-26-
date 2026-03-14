# Ex.No:4(E) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:
To implement the Memento Design Pattern that allows saving and restoring versions of an Article object.

## ALGORITHM :
1.	Create ArticleMemento to store article content (state).
2.	Create Article (Originator) that can write, save, and restore content.
3.	Create VersionHistory (Caretaker) to store multiple mementos.
4.	Allow the user to:
5.	Write new content
6.	Save current version
7.	View all saved versions
8.	Restore any version
9.	Display restored version content.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:
```
import java.util.*;

class Article {
    private String content;

    public void setContent(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }

    public ArticleMemento save() {
        return new ArticleMemento(content);
    }

    public void restore(ArticleMemento memento) {
        this.content = memento.getContent();
    }
}

class ArticleMemento {
    private final String content;

    public ArticleMemento(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }
}

class ArticleHistory {
    private List<ArticleMemento> versions = new ArrayList<>();

    public void saveVersion(Article article) {
        versions.add(article.save());
    }

    public ArticleMemento getVersion(int index) {
        if (index >= 0 && index < versions.size()) {
            return versions.get(index);
        }
        return null;
    }
}

public class ArticleManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Article article = new Article();
        ArticleHistory history = new ArticleHistory();

        int n = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < n; i++) {
            String content = sc.nextLine();
            article.setContent(content);
            history.saveVersion(article);
        }

        int restoreIndex = Integer.parseInt(sc.nextLine());
        ArticleMemento m = history.getVersion(restoreIndex);
        if (m != null) {
            article.restore(m);
            System.out.println(article.getContent());
        } else {
            System.out.println("Invalid version");
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="725" height="517" alt="image" src="https://github.com/user-attachments/assets/ab909229-c9d4-4a9e-b05e-bdfae6a49b4b" />


## RESULT:
Thus, the program successfully demonstrates the Memento Pattern, allowing the user to save, view, and restore different versions of an article.




