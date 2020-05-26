FROM pandoc/latex:latest

RUN apk add --no-cache bash \
                       coreutils \
                       grep \
                       sed \
                       git \
                       curl \
                       wget \
                       jq


RUN tlmgr install adjustbox \
                  babel-german \
                  background \
                  bidi \
                  collectbox \
                  csquotes \
                  everypage \
                  filehook \
                  footmisc \
                  footnotebackref \
                  framed \
                  fvextra \
                  letltxmacro \
                  ly1 \
                  mdframed \
                  mweights \
                  needspace \
                  pagecolor \
                  sourcecodepro \
                  sourcesanspro \
                  titling \
                  ucharcat \
                  ulem \
                  unicode-math \
                  upquote \
                  xecjk \
                  xurl \
                  zref \
                  fdsymbol \
                  pgf \
                  pgfplots

RUN git clone https://github.com/codimd/cli
