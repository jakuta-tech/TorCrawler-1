
**Table of Contents**  *generated with [DocToc](http://doctoc.herokuapp.com/)*

- [TorCrawler](#)
		- [Simple](#)
		- [Reliable](#)
		- [Flexible](#)
		- [Efficient](#)
	- [Installation](#)
		- [Dependency](#)
	- [Usage](#)
	- [Contributing](#)
	- [History](#)
	- [Credits](#)
	- [License](#)

# TorCrawler
TorCrawler is single machine based web page crawler. It aims to be simple, reliable, fexlible and efficient.

### Simple
Most of it is coded by Perl, hence the code is concise. The core function only includes three files, Fetcher.pl, PageParser.pl and TorGet.php, resulting less than 400 total number of lines. 

### Reliable
All intermediate files are kept under a single folder. The cralwer threads work jointly in a map-reduce manner. As individual crawler agent is realized by process, crash of agents does not suspend the main program and the unfinished work will be reassigned in the coming round. The whole program is rather robust - it can be stopped and resumed any time and the results will stay intact.

### Flexible
It's higly customizable to your task. This means, first, you can specify the link following rules simply by a regular expression based file; second, you can plugin your own parser to extract information from the crawled html content. There is a Perl parser template you can follow. 

### Efficient
With Tor proxy technique, it can crawl urls with concurrent threads from multiple distinct IP addresses and more importantly, all this can be done on a single machine with a single IP address. Tor proxy helps unleash all your bandwidth and dismiss your concern of crawling speed limited by single IP. With tor, you can literally own as many virtual machines as you want, simply by a command line argument! The crawler scores each proxy based on the downloading speed and error rate and works with top ranked proxy candidates over time.  

## Installation
### Dependency
1. Multi-TOR, script that boots multiple Tor proxies on your machine. It can be downloaded from  https://github.com/jseidl/Multi-TOR. It should be fairly straightfoward to use it by following the instruction.

2. Perl and PHP language support and their related packages

  2.1 Perl 
  
  Getopt::Long, Data::Dumper, Digest:MD5, FindBin, File::Basename, Try::Tiny, JSON, pQuery, HTML::LinkExtractor. Install them through cpan
  
  2.2 PHP
  
  curl
  



## Usage

TODO: Write usage instructions

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

TODO: Write history

## Credits

TODO: Write credits

## License

TODO: Write license
