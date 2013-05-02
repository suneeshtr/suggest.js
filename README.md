suggest.js
==========

A library that generates a list of word suggestions from an input string.

# Usage #

### Initialize ###
	var words = ["koala", "koangaroo", "teddy", "teddybear"]
	var auto = new Suggester(words)

### Suggestions for input "ko" ###
	var matches = auto.suggest("ko")
	-> matches = ["koala", "koangaroo"]

### Suggestions for input "te" ###
	matches = auto.suggest("te")
	-> matches = ["teddy", "teddybear"]

### Suggestions for input "teddyb" ###
	matches = auto.suggest("teddyb")
	-> matches = ["teddybear"]

### Suggestions for input "xyz". No matches returns null ###
	matches = auto.suggest("xyz")
	-> matches = null

### Load new list into object ###
	words = ["xyzabc", koala", "koangaroo", "teddy", "teddybear"]
	auto.load(words)
	matches = auto.suggest("xyz")
	-> matches = ["xyzabc"]
