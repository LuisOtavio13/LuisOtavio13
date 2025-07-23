# 👋 Hello, I'm Luis otavio

💻 Programming Student | 🌍 Passionate About Technology  

## 🚀 Programming Languages  
[![My Skills](https://skillicons.dev/icons?i=java,python,javascript,c)](https://skillicons.dev)  

## 🛠️ Tools & Technologies  
[![My Skills](https://skillicons.dev/icons?i=vscode,mysql,bootstrap,git,github)](https://skillicons.dev)  

## 📫 Contact  

[![Gmail Badge](https://img.shields.io/badge/-YourEmail-006bed?style=flat-square&logo=Gmail&logoColor=white&link=mailto:YourEmail)](mailto:YourEmail)  


![DiasEllen26 GitHub stats](https://github-readme-stats.vercel.app/api?username=LuisOtavio13&show_icons=true&theme=radical)  

```java
/**
 * MyProfile class showing my programming preferences
 */
public class MyProfile {
    // Fields
    private String name;
    private String favoriteLanguage;
    private String currentLearning;
    
    // Constructor
    public MyProfile(String name, String favoriteLanguage, String currentLearning) {
        this.name = name;
        this.favoriteLanguage = favoriteLanguage;
        this.currentLearning = currentLearning;
    }
    
    // Getters and Setters
    public String getName() {
        return name;
    }
    
    public String getFavoriteLanguage() {
        return favoriteLanguage;
    }
    
    public void setFavoriteLanguage(String language) {
        this.favoriteLanguage = language;
    }
    
    public String getCurrentLearning() {
        return currentLearning;
    }
    
    // Display method
    public void showProfile() {
        System.out.println("===== MY PROFILE =====");
        System.out.println("Name: " + name);
        System.out.println("Favorite Language: " + favoriteLanguage);
        System.out.println("Currently Learning: " + currentLearning);
        System.out.println("=====================");
    }
    
    // Main method
    public static void main(String[] args) {
        MyProfile myProfile = new MyProfile(
            "Luis Otavio", 
            "Java", 
            "Spring Framework and C"
        );
        myProfile.showProfile();
    }
}
