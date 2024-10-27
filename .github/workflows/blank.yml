import java.util.*;
import java.net.URL;

class Post {
    private String title;
    private String content;
    private URL url;

    public Post(String title, String content, URL url) {
        this.title = title;
        this.content = content;
        this.url = url;
    }

    public String getTitle() { return title; }
    public String getContent() { return content; }
    public URL getUrl() { return url; }

    @Override
    public String toString() {
        return "Title: " + title + "\nContent: " + content + "\nURL: " + url;
    }
}

class PostManager {
    private List<Post> posts;

    public PostManager() {
        this.posts = new ArrayList<>();
    }

    public void addPost(Post post) {
        posts.add(post);
    }

    public void deletePost(int index) {
        if (index >= 0 && index < posts.size()) {
            posts.remove(index);
        } else {
            System.out.println("Invalid post index.");
        }
    }

    public void listPosts() {
        for (int i = 0; i < posts.size(); i++) {
            System.out.println("Post #" + i);
            System.out.println(posts.get(i));
            System.out.println("--------------------");
        }
    }
}

public class PostManagementProgram {
    private static PostManager postManager = new PostManager();
    private static Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        while (true) {
            System.out.println("\n1. Add Post\n2. Delete Post\n3. List Posts\n4. Exit");
            System.out.print("Enter your choice: ");
            int choice = scanner.nextInt();
            scanner.nextLine();  // Consume newline

            switch (choice) {
                case 1:
                    addPost();
                    break;
                case 2:
                    deletePost();
                    break;
                case 3:
                    postManager.listPosts();
                    break;
                case 4:
                    System.out.println("Exiting program. All posts will be deleted.");
                    System.exit(0);
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        }
    }

    private static void addPost() {
        try {
            System.out.print("Enter post title: ");
            String title = scanner.nextLine();
            System.out.print("Enter post content: ");
            String content = scanner.nextLine();
            System.out.print("Enter URL: ");
            String urlString = scanner.nextLine();
            URL url = new URL(urlString);

            Post post = new Post(title, content, url);
            postManager.addPost(post);
            System.out.println("Post added successfully.");
        } catch (Exception e) {
            System.out.println("Error adding post: " + e.getMessage());
        }
    }

    private static void deletePost() {
        System.out.print("Enter the index of the post to delete: ");
        int index = scanner.nextInt();
        postManager.deletePost(index);
    }
}
