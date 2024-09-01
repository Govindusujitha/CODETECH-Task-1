# CODETECH-Task-1architecture behaviour of  is
begin
    process

    begin

        wait;
    end process;
end behaviour;
module adder(sum, cout, a, b, cin);
    input a, b, cin;
    output cout, sum;

    assign sum = a ^ b ^ cin;
    assign cout = (a & b) | (cin & (a | b));
endmodule

D Flip-Flop:
verilog
module D_FF(q, d, rst_n, clk, init_value);
    output reg q;
    input d, rst_n, clk, init_value;

    always @(posedge clk or negedge rst_n) begin
        if (~rst_n)
            q <= init_value;
        else
            q <= d;
    end
endmodule

VHDL Examples
AND Gate:
vhdl
library IEEE;
use IEEE.std_logic_1164.all;

entity andGate is
    port(A : in std_logic;
         B : in std_logic;
         Y : out std_logic);
end andGate;

architecture andLogic of andGate is
begin
    Y <= A AND B;
end andLogic;

OR Gate:
vhdl
library IEEE;
use IEEE.std_logic_1164.all;

entity orGate is
    port(A : in std_logic;
         B : in std_logic;
         Y : out std_logic);
end orGate;

architecture orLogic of orGate is
begin
    Y <= A OR B;
end orLogic
