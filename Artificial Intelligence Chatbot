import java.util.*;

class Chatbot {

    private Map<String, String> knowledgeBase;

    public Chatbot() {

        knowledgeBase = new HashMap<>();

        // Frequently Asked Questions
        knowledgeBase.put("hello", "Hello! How can I help you?");
        knowledgeBase.put("hi", "Hi! Nice to meet you.");
        knowledgeBase.put("how are you", "I'm doing great. Thanks for asking!");
        knowledgeBase.put("your name", "I'm Java AI Chatbot.");
        knowledgeBase.put("java", "Java is an object-oriented programming language.");
        knowledgeBase.put("oop", "OOP stands for Object-Oriented Programming.");
        knowledgeBase.put("python", "Python is a popular programming language used in AI.");
        knowledgeBase.put("ai", "Artificial Intelligence enables machines to simulate human intelligence.");
        knowledgeBase.put("nlp", "Natural Language Processing helps computers understand human language.");
        knowledgeBase.put("bye", "Goodbye! Have a great day.");
    }

    public String getResponse(String input) {

        input = input.toLowerCase();

        for (String keyword : knowledgeBase.keySet()) {
            if (input.contains(keyword)) {
                return knowledgeBase.get(keyword);
            }
        }

        return "Sorry, I don't understand. Can you ask something else?";
    }

    // Add new knowledge (training)
    public void train(String question, String answer) {
        knowledgeBase.put(question.toLowerCase(), answer);
    }
}

public class AIChatbot {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        Chatbot bot = new Chatbot();

        System.out.println("==================================");
        System.out.println("      JAVA AI CHATBOT");
        System.out.println("Type 'exit' to quit.");
        System.out.println("==================================");

        while (true) {

            System.out.print("\nYou: ");

            String userInput = sc.nextLine();

            if (userInput.equalsIgnoreCase("exit")) {
                System.out.println("Bot: Goodbye!");
                break;
            }

            System.out.println("Bot: " + bot.getResponse(userInput));
        }

        sc.close();
    }
}
