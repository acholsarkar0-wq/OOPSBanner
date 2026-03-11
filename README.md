import java.util.HashMap;
import java.util.Map;

public class OOPSBannerUC8 {

    // HashMap to store patterns
    private static Map<Character, String[]> patternMap = new HashMap<>();

    // Function to load patterns
    public static void loadPatterns() {

        patternMap.put('O', new String[]{
                " *** ",
                "*   *",
                "*   *",
                "*   *",
                " *** "
        });

        patternMap.put('P', new String[]{
                "**** ",
                "*   *",
                "**** ",
                "*    ",
                "*    "
        });

        patternMap.put('S', new String[]{
                " ****",
                "*    ",
                " *** ",
                "    *",
                "**** "
        });
    }

    // Function to render banner
    public static void renderBanner(String word) {

        int height = 5;

        for (int i = 0; i < height; i++) {

            for (char ch : word.toCharArray()) {

                String[] pattern = patternMap.get(Character.toUpperCase(ch));

                if (pattern != null) {
                    System.out.print(pattern[i] + "  ");
                } else {
                    System.out.print("     ");
                }
            }

            System.out.println();
        }
    }

    public static void main(String[] args) {

        loadPatterns();

        String word = "OOPS";

        renderBanner(word);
    }
}
