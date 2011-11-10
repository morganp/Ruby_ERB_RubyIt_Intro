!SLIDE
# RubyIt #

Create scalable.v from scalable.rv

    $ ruby_it --parameter CHANNELS=4 \
        --file scalable.rv

    >"CHANNELS=4"
    >File: scalable.rv Output: ./

!SLIDE
# Generated Output #
.notes Generated into scalable.v

.notes  @@@ verilog

    module scalable (
      rx_0,
      rx_1,
      rx_2,
      rx_3,
      clk,
      rst_an
    );
    
    endmodule

!SLIDE
# RubyIt #

Installation

    gem install ruby_it

Usage

    $ ruby_it --help
    Common options:
    -h, --help                       Show this message
        --version                    Show version
    -f, --file input_filename        Input source file to evaluate

Specific options:
    -v, --[no-]verbose               Run Verbosely
    -q, --quiet                      Run Quiet, not Verbose
        --parameter param            Command line parameters (Override data file settings)    -c, --config config_data         Load Config File
    -p, --outpath output_path        Redirect generated file output
    -o, --out output_filename        Define different generated filename from source file 

!SLIDE
# RubyIt Features  

Better white space control

.notes Remove trailing white space including line returns

    <% -%> 


!SLIDE
# Further Reading (1)#
![Programming Ruby](pickaxe.png)
## Programming Ruby ##
ISBN 978-1934356081

!SLIDE
# Further Reading (2)#
![The Ruby Way](rubyway.png)
## The Ruby Way ##
ISBN 978-0672328848

!SLIDE
# In Depth Articles #
[Practising Ruby](http://practicingruby.com/)

# Latest News #
[Ruby Flow](http://www.rubyflow.com/)  
[Ruby Inside](http://www.rubyinside.com/)

