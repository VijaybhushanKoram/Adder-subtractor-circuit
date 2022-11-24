`timescale 1ns / 1ps

////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer:
//
// Create Date:   18:42:01 11/24/2022
// Design Name:   jbh
// Module Name:   C:/Users/VIJAY//GITHUB VERILOG/adsb/jbhtb.v
// Project Name:  adsb
// Target Device:  
// Tool versions:  
// Description: 
//
// Verilog Test Fixture created by ISE for module: jbh
//
// Dependencies:
// 
// Revision:
// Revision 0.01 - File Created
// Additional Comments:
// 
////////////////////////////////////////////////////////////////////////////////

module jbhtb;

	// Inputs
	reg [3:0] a;
	reg [3:0] b;
	reg cin;

	// Outputs
	wire [3:0] k;
	wire z1;
	wire z2;
	wire z3;
	wire z4;

	// Instantiate the Unit Under Test (UUT)
	jbh uut (
		.a(a), 
		.b(b), 
		.k(k), 
		.cin(cin), 
		.z1(z1), 
		.z2(z2), 
		.z3(z3), 
		.z4(z4)
	);

	initial begin
		
        a=4'b0010;
        b=4'b0100;
        cin=0;
        #10
        a=4'b0011;
        b=4'b1100;
        cin=0;
        #10;
        a=4'b0100;
        b=4'b0111;
        cin=1;
        #10;
		  
        
        $finish;
		// Add stimulus here

	end
      
endmodule

