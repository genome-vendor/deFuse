###################################################
#
# Makefile for tools
# Creator [Xcode -> Makefile Ver: Feb 14 2007 09:18:41]
# Created: [Tue Aug 10 13:19:17 2010]
#
###################################################

#
# Macros
#

BAMTOOLSDIR = ../external/BamTools
BAMTOOLSLIB = libbamtools.a

INCLUDE = -I/usr/include/bam -I. -I${BAMTOOLSDIR}
CC = /usr/bin/g++
CXX = /usr/bin/g++
CXXFLAGS = -O3 -DDEBUG_CHECKS $(INCLUDE)
LDFLAGS = -O3
LDLIBS = -lbam -lz -L$(BAMTOOLSDIR) -lbamtools

all: tools 


# 

$(BAMTOOLSDIR)/$(BAMTOOLSLIB) :
		$(MAKE) --no-print-directory -C $(BAMTOOLSDIR) $(BAMTOOLSLIB)

#
# Build tools
#

clustermatepairs_stdin : \
		./Common.o\
		./DebugCheck.o\
		./MatePairEM.o\
		./asa136.o\
		./asa241.o\
		./clustermatepairs_stdin.o\
		$(BAMTOOLSDIR)/$(BAMTOOLSLIB)

clustermatepairs : \
		./AlignmentStream.o\
		./Common.o\
		./DebugCheck.o\
		./MatePairEM.o\
		./asa136.o\
		./asa241.o\
		./clustermatepairs.o\
		$(BAMTOOLSDIR)/$(BAMTOOLSLIB)

setcover: \
		./Common.o\
		./DebugCheck.o\
		./Parsers.o\
		./setcover.o\
		$(BAMTOOLSDIR)/$(BAMTOOLSLIB)

initsplitalign: \
		./AlignmentStream.o\
		./FastaIndex.o\
		./Common.o\
		./DebugCheck.o\
		./ExonRegions.o\
		./ReadIndex.o\
		./SplitAlignment.o\
		./SplitReadAligner.o\
		./Parsers.o\
		./initsplitalign.o\
		$(BAMTOOLSDIR)/$(BAMTOOLSLIB)

dosplitalign: \
		./AlignmentStream.o\
		./FastaIndex.o\
		./Common.o\
		./DebugCheck.o\
		./ExonRegions.o\
		./ReadIndex.o\
		./SplitAlignment.o\
		./SplitReadAligner.o\
		./Parsers.o\
		./ReadStream.o\
		./dosplitalign.o\
		$(BAMTOOLSDIR)/$(BAMTOOLSLIB)

evalsplitalign: \
		./AlignmentIndex.o\
		./FastaIndex.o\
		./Common.o\
		./DebugCheck.o\
		./ExonRegions.o\
		./ReadIndex.o\
		./SplitAlignment.o\
		./SplitReadAligner.o\
		./ReadStream.o\
		./evalsplitalign.o\
		$(BAMTOOLSDIR)/$(BAMTOOLSLIB)

splitseq: \
		./AlignmentStream.o\
		./FastaIndex.o\
		./Common.o\
		./DebugCheck.o\
		./ExonRegions.o\
		./ReadIndex.o\
		./SplitAlignment.o\
		./SplitReadAligner.o\
		./Parsers.o\
		./PathFinder.o\
		./splitseq.o\
		$(BAMTOOLSDIR)/$(BAMTOOLSLIB)

denovoseq: \
		./AlignmentIndex.o\
		./ReadIndex.o\
		./FastaIndex.o\
		./Common.o\
		./DebugCheck.o\
		./ExonRegions.o\
		./SplitReadAligner.o\
		./Parsers.o\
		./PathFinder.o\
		./DeNovoFusion.o\
		./denovoseq.o\
		$(BAMTOOLSDIR)/$(BAMTOOLSLIB)

calccov: \
		./AlignmentStream.o\
		./Common.o\
		./DebugCheck.o\
		./ExonRegions.o\
		./calccov.o\
		$(BAMTOOLSDIR)/$(BAMTOOLSLIB)

estislands : \
		./estislands.o\
		./EstCatalog.o\
		$(BAMTOOLSDIR)/$(BAMTOOLSLIB)

localalign : \
		./localalign.o\
		./SimpleAligner.o\
		./DebugCheck.o\
		./Common.o

matealign : \
		./matealign.o\
		./Common.o\
		./DebugCheck.o\
		./ReadStream.o\
		./Sequences.o\
		./SimpleAligner.o

tools : clustermatepairs setcover calccov estislands initsplitalign dosplitalign evalsplitalign localalign splitseq matealign
	

clean : 
		rm -f *.o
