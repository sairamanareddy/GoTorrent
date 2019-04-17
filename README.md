# GoTorrent
[![CircleCI](https://circleci.com/gh/sairamanareddy/GoTorrent.svg?style=svg)](https://circleci.com/gh/sairamanareddy/GoTorrent) [![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/IITH-SBJoshi/concurrency-8/blob/master/LICENSE) [![GoDoc](https://godoc.org/github.com/narqo/go-badge?status.svg)](https://sairamanareddy.github.io/GoTorrent/pkg/github.com/concurrency-8/)
 
Bit-torrent client implementation as part of CS2433 (Principles of Programming Language II ) by Prof. Saurabh Joshi .

* [Description](#description)
* [Documentation](#Documentation)
* [Setup](#Setup)
* [Usage](#Usage)
* [Guidelines for contribution](#guidelines-for-contribution)
* [External packages](#external-packages)
* [Resources and References](#Resources-and-References)

## Description
1. **Objective**
	- Get familiar with writing concurrent programs.
	- Using software technologies like Continous Integration, Unit Testing, Documentation.
2. **Features**
	- Downloading multiple torrent files concurrently.
	- Fetching Peer lists from both HTTP and UDP Trackers.
	- Fetching pieces of blocks concurrently from Peers.
	- Enabling Resume capabilities on abrupt termination.
	- Generating detailed log files for debugging.
	- A command line interface for managing.
3. **Team**
	- Shraiysh Gupta (CS17BTECH11050)
	- Puneet Mangla (CS17BTECH11029)
	- Lingam Sai Ramana Reddy (CS17BTECH11022)
	- Hitesh (MA17BTECH11004)

## Documentation
1. You can refer to [this](https://iith-sbjoshi.github.io/concurrency-8/pkg/github.com/concurrency-8) to see the documentation generated for the master branch.

## Setup
1. **Installing Golang**
	- Follow [this](https://golang.org/doc/install) link **OR**
	- Run ```sudo apt-get install golang```
	- Set the environment variables `GOPATH` and `GOBIN` as follows :
		- ```GOPATH="$HOME/go"```
		- ```GOBIN="$GOPATH/bin"```
		- ```PATH=$PATH:$GOBIN```
2. **Building**
	
	Get [dep](https://github.com/golang/dep) for installing the dependencies
	```
	$ cd $GOPATH/src/github.com # Come to the appropriate directory
	$ git clone https://github.com/IITH-SBJoshi/concurrency-8.git
	$ cd concurrency-8/
	$ dep ensure		# Get the dependencies
	$ ./build.sh    	# To check if all tests passes
	```
## Usage
1. **Downloading**
	- ```go run main.go --files File1 File2 File3 -v -d ../../```
2. **Flags**

| __Flag Name__ | __Description__ | __Default__ |
|-------------|------------|------------|
| ```--files [path] [path] ...``` |  List of Torrent Files | empty |
| ```--download -d```  | Specify the download path for downloading the files.| "" |
| ```--rescap -rc```  | True if pause and resume feature is needed. False otherwise. | false |
| ```--resume -r```  | True to resume partially downloaded files. | false |
| ```--help```  | Print this help message and exit. |- |
| ```--verbose -v```  | True if misc output is required. False otherwise. | false |

### External Packages
- [github.com/zeebo/bencode](https://github.com/zeebo/bencode/blob/master/LICENSE)
- [github.com/alecthomas/gometalinter](https://github.com/alecthomas/gometalinter/blob/master/COPYING)
- [golang.org/x/lint/golint](https://github.com/golang/lint/blob/master/LICENSE)
- [github.com/gojp/goreportcard](https://github.com/gojp/goreportcard/blob/master/LICENSE)
- [github.com/stretchr/testify](https://github.com/stretchr/testify/blob/master/LICENSE)
- [github.com/sethgrid/multibar](https://github.com/sethgrid/multibar/blob/master/LICENSE.md)
- [github.com/fzipp/gocyclo](https://github.com/fzipp/gocyclo/blob/master/LICENSE)
- [github.com/client9/misspell/cmd/misspell](https://github.com/client9/misspell/blob/master/LICENSE)
- [github.com/gordonklaus/ineffassign](https://github.com/gordonklaus/ineffassign/blob/master/LICENSE)

### Resources and References
- [Bittorent Specifications](http://jonas.nitro.dk/bittorrent/bittorrent-rfc.html)
- [Bittorent Specifications](http://www.bittorrent.org/beps/bep_0003.html)
- [Bittorrent in Javascript](https://allenkim67.github.io/programming/2016/05/04/how-to-make-your-own-bittorrent-client.html)
