!SLIDE
# ERB: Embedded Ruby #

    @@@ ruby
    <% a=12 %>
    <% b=20 %>

This could be written as:

    <% a = 10
       b = 20 %>

To generate output
.notes equivalent of puts in scripts

    <%= a %>

!SLIDE
# ERB and Templates #
Dynamic port lists can be created

    @@@ ruby
    module scalable (
    <% (0...CHANNELS).each do |i| -%>
      rx_<%= i %>,
    <% end -%>
      clk,
      rst_an
    );
    
    endmodule
