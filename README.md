public class OopsBannerUC4 {

    public static void main(String[] args) {

        // Store banner lines in a String array
        String[] banner = {
                String.join(" ", "OOOOO", " ", "OOOOO", " ", "PPPPP", " ", "SSSSS"),
                String.join(" ", "O", "   ", "O", "   ", "P", "   ", "P", "   ", "S"),
                String.join(" ", "O", "   ", "O", "   ", "PPPPP", " ", "SSSSS"),
                String.join(" ", "O", "   ", "O", "   ", "P", "   ", " ", "   ", "S"),
                String.join(" ", "OOOOO", " ", "OOOOO", " ", "P", " ", "SSSSS")
        };

        // Print banner using loop
        for (String line : banner) {
            System.out.println(line);
        }
    }
}
