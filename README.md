public class OopsBannerUC5 {

    public static void main(String[] args) {

        // Array declaration and initialization in a single statement
        String[] banner = {
                String.join(" ", "OOOOO", " ", "OOOOO", " ", "PPPPP", " ", "SSSSS"),
                String.join(" ", "O", "   ", "O", "   ", "P", "   ", "P", "   ", "S"),
                String.join(" ", "O", "   ", "O", "   ", "PPPPP", " ", "SSSSS"),
                String.join(" ", "O", "   ", "O", "   ", "P", "   ", " ", "   ", "S"),
                String.join(" ", "O", "   ", "O", "   ", "P", "   ", " ", "   ", "S"),
                String.join(" ", "O", "   ", "O", "   ", "P", "   ", "P", "   ", "S"),
                String.join(" ", "OOOOO", " ", "OOOOO", " ", "P", " ", "SSSSS")
        };

        // Print banner using enhanced for loop
        for (String line : banner) {
            System.out.println(line);
        }
    }
}
