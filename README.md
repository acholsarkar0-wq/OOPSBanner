import java.util.HashMap;
import java.util.Map;

public class OOPSBannerUC7 {

    // Static Inner Class to store Character and Pattern
    static class CharacterPattern {
        private char character;
        private String[] pattern;

        public CharacterPattern(char character, String[] pattern) {
            this.character = character;
            this.pattern = pattern;
        }

        public char getCharacter() {
            return character;
        }

        public String[] getPattern() {
            return pattern;
        }
    }

    // Character Pattern Map
    static class CharacterPatternMap {
        private static Map<Character, CharacterPattern> patternMap = new HashMap<>();

        static {
            patternMap.put('O', new CharacterPattern('O', new String[]{
                    " *** ",
                    "*   *",
                    "*   *",
                    "*   *",
                    " *** "
            }));

            patternMap.put('P', new CharacterPattern('P', new String[]{
                    "**** ",
                    "*   *",
                    "**** ",
                    "*    ",
                    "*    "
            }));

            patternMap.put('S', new CharacterPattern('S', new String[]{
                    " ****",
                    "*    ",
                    " *** ",
                    "    *",
                    "**** "
            }));
        }

        public static CharacterPattern getPattern(char ch) {
            return patternMap.get(ch);
        }
    }

    public static void main(String[] args) {

        String bannerText = "OOPS";
        int height = 5;

        for (int i = 0; i < height; i++) {

            StringBuilder line = new StringBuilder();

            for (char ch : bannerText.toCharArray()) {
                CharacterPattern pattern = CharacterPatternMap.getPattern(ch);

                if (pattern != null) {
                    line.append(pattern.getPattern()[i]).append("  ");
                }
            }

            System.out.println(line);
        }
    }
}
