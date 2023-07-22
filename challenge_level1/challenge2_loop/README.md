

#challenge level1 : challenge2_loop

in this case there was infinite loop due to the code was not checking if we tested all the case if its over jump and exit, also consider if the test passed or failed which was not testing properly

loop:
  li t6,1
  beq x0, t5, over
  sub t5,t5,t6
	lw t1, (t0)
  lw t2, 4(t0)
  lw t3, 8(t0)
  add t4, t1, t2
  addi t0, t0, 12
  bne t3, t4, fail
  j loop
over:j pass  

changed code to check if the loop counter over , or the test passsed all case or test any of the on case failed and take correct action
