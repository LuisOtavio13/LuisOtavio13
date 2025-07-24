<div align="center">
  <img src="https://media.giphy.com/media/L1R1tvI9svkIWwpVYr/giphy.gif" width="200px">
  <h1>✨ Luis Otavio ✨</h1>
  <h3>Java and C Developer in Training</h3>
  
  <div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=1000&color=7A3CE7&center=true&vCenter=true&width=435&lines=Welcome+to+my+GitHub+profile!;Java+%7C+Python+%7C+JavaScript+%7C+C;Always+learning+new+things!" alt="Typing SVG" />
</div>
</div>

---

## 🛠️ Tech Stack Avançada

<div align="center">
  
  ### 🧠 Main Languages
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
  <img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white">
  
  ### �‍💻 Frameworks & Libraries
  <img src="https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white">
  <img src="https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white">
  
  ### 🗃️ Databases
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
  
  ### ⚙️ Tools
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white">
  <img src="https://img.shields.io/badge/IntelliJ_IDEA-000000?style=for-the-badge&logo=intellij-idea&logoColor=white">
</div>

---

## 📊 GitHub Analytics Pro

<div align="center">
  
  ![Estatísticas](https://github-readme-stats.vercel.app/api?username=LuisOtavio13&show_icons=true&theme=merko&include_all_commits=true&count_private=true&line_height=40)
  
  ![Linguagens Top](https://github-readme-stats.vercel.app/api/top-langs/?username=LuisOtavio13&theme=merko&layout=compact&langs_count=6)
  
  ![Troféus](https://github-profile-trophy.vercel.app/?username=LuisOtavio13&theme=onestar&row=2&column=3&margin-w=15)
  
  ![Streak](https://github-readme-streak-stats.herokuapp.com/?user=LuisOtavio13&theme=merko)
</div>

---

## 🎯 Projeto Destaque

[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=LuisOtavio13&repo=github-explorer-framework&theme=merko)](https://github.com/LuisOtavio13/github-explorer-framework)

---

## 💎 Classe Java Premium

```java

public class DevProfile {
    
   
    public enum SkillLevel { BEGINNER, INTERMEDIATE, ADVANCED }
    public enum DevType { FRONTEND, BACKEND, FRONTEND, PENTERSTER }
    
   
    private static DevProfile instance;
    
    
    public static class Builder {
        private String name;
        private DevType type;
        private Map<String, SkillLevel> skills = new HashMap<>();
        private List<String> tools = new ArrayList<>();
        
        public Builder(String name) {
            this.name = name;
        }
        
        public Builder setType(DevType type) {
            this.type = type;
            return this;
        }
        
        public Builder addSkill(String skill, SkillLevel level) {
            this.skills.put(skill, level);
            return this;
        }
        
        public Builder addTool(String tool) {
            this.tools.add(tool);
            return this;
        }
        
        public DevProfile build() {
            return new DevProfile(this);
        }
    }
    
   
    private final String name;
    private final DevType type;
    private final Map<String, SkillLevel> skills;
    private final List<String> tools;
    
    
    private DevProfile(Builder builder) {
        this.name = builder.name;
        this.type = builder.type;
        this.skills = Collections.unmodifiableMap(new HashMap<>(builder.skills));
        this.tools = Collections.unmodifiableList(new ArrayList<>(builder.tools));
    }
    
   
    public static DevProfile getInstance(Builder builder) {
        if(instance == null) {
            instance = builder.build();
        }
        return instance;
    }
    
    
    public String getName() { return name; }
    public DevType getType() { return type; }
    public Map<String, SkillLevel> getSkills() { return skills; }
    public List<String> getTools() { return tools; }
    
    
    public void displayProfile() throws InterruptedException {
        System.out.println("\n\n");
        printWithDelay("   Name: " + name, 100);
        printWithDelay("   Type: " + type.toString(), 100);
        
        System.out.println("   Skills:");
        skills.forEach((skill, level) -> {
            printWithDelay("    ▸ " + skill + " - " + level, 50);
        });
        
        System.out.println("   Tools:");
        tools.forEach(tool -> {
            printWithDelay("    ▸ " + tool, 30);
        });
        
       
        System.out.println("\n\n");
    }
    
    private void printWithDelay(String text, int delay) {
        try {
            Thread.sleep(delay);
            System.out.println(text);
        } catch (InterruptedException e) {
            Thread.currentThread().interrupt();
        }
    }
    
   
    public static void main(String[] args) throws InterruptedException {
        DevProfile profile = DevProfile.getInstance(
            new DevProfile.Builder("Luis Otavio")
                .setType(DevType.BACKEND)
                .addSkill("Java", SkillLevel.INTERMEDIATE)
                .addSkill("Python", SkillLevel.ADVANCED)
                .addSkill("JavaScript", SkillLevel.INTERMEDIATE)
                .addTool("IntelliJ IDEA")
                .addTool("VS Code")
                .addTool("Git")
        );
        
        profile.displayProfile();
    }
}
