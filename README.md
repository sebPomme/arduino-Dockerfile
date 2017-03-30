# Arduino Dockerfile

## Description

A Dockerfile for containerising Arduino sketches, and uploading them into your Arduino Boards. [Instructions on how to deploy a docker container to your Arduino board can be found here](http://reprage.com/post/how-to-deploy-docker-containers-to-an-arduino/).

A Vagrantfile configuration has been added, as well as a customized docker host configuration. Vagrant will error the first time it provisions its docker host. This is a workaround for the path.

Be sure to update the -m flag to ino for your board.

vagrant docker-run default -- ino upload -m boardId

Will compile and upload your sketch if everything is working.

## License

Copyright 2015, Clinton Freeman

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
