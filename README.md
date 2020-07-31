# builder-wire

Console Application Usage:
BuilderWireCodingChallenge /w:{words filename} /a:{article filename} /out:{output filename}
/out parameter is Optional, outputs to screen when not supplied

Class Usage:
using WordMatch;


WordMatcher wordMatcher = new WordMatcher(wordsFilename, articleFilename);
//or
//string[] words = { "the","quick",...,"dog" };
//string article = "the quick brown fox jumps over the lazy dog.";
//WordMatcher wordMatcher = new WordMatcher(words,article);
var dict = wordMatcher.ProcessToDictionary();
string[] contents = WordMatcher.ToLetterBulletedList(dict);

Assumptions based on the input files provided:
1. Every word in {article file/string parameter} should have a corresponding entry in {words files/string[] words}.
2. {words file} should have a line break per word as per sample input file.
