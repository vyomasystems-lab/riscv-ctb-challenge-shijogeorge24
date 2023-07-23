challenge_level1:challenge3_illegal

When ever an expection occur corresponding trap will call.
We can write the address we wanna jump when ever an expection occur is by doing 
following step
  #la t2,mtvec_handler
  load adress to t2 register

  #csrw mtvec,t2
  write that adress to mtvec register

  once we reached the trap we have to read the csrr with macuse which will return the information about what kind of exception occured
  in our case it was illegal expection . once we read that just check if it matches to the exception we ware excepting if it matches , get the adress where the exception coccured and increment it to next adress we are done with it 

  this can be achived by adding 4 to the conent of mepc the mret wich will be next instruction

  issue with code

  it was not adding 4 to mepc register before return before jumping back