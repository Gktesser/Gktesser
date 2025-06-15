## Hi there 👋

// semáforo 1
#define vm1    13
#define am1    12
#define vd1    11

// semáforo pedestre 1
#define vmpd1  10
#define vdpd1   9

// semáforo 2
#define vm2     8
#define am2     7
#define vd2     6

// semáforo pedestre 2
#define vmpd2   5
#define vdpd2   4

void setup() {
  pinMode(vm1, OUTPUT);
  pinMode(am1, OUTPUT);
  pinMode(vd1, OUTPUT);
  pinMode(vmpd1, OUTPUT);
  pinMode(vdpd1, OUTPUT);
  pinMode(vm2, OUTPUT);
  pinMode(am2, OUTPUT);
  pinMode(vd2, OUTPUT);  
  pinMode(vmpd2, OUTPUT);  
  pinMode(vdpd2, OUTPUT);
}

void loop() {
  atualizarSemaforos();
}

void atualizarSemaforos() {
  setLeds(true, false, false, // semáforo 1
          false, true,   // semáforo pedestre 1
          false, false, true, // semáforo 2
          true, false,   // semáforo pedestre 2
          4);                                

  setLeds(true, false, false,
          false, true,   
          false, true, false,
          true, false,   
          2);                                

  setLeds(false, false, true, 
          true, false,  
          true, false, false,
          false, true,   
          4);                                

  setLeds(false, true, false,
          true, false,   
          true, false, false,
          false, true,   
          2);                                
}

void setLeds(bool vm1_state, bool am1_state, bool vd1_state, bool vmpd1_state, bool vdpd1_state,
             bool vm2_state, bool am2_state, bool vd2_state, bool vmpd2_state, bool vdpd2_state,
             int tempo_segundos) {
  //Via 1
  digitalWrite(vm1, vm1_state);
  digitalWrite(am1, am1_state);
  digitalWrite(vd1, vd1_state);
  digitalWrite(vmpd1, vmpd1_state);
  digitalWrite(vdpd1, vdpd1_state);
  
  //Via 2
  digitalWrite(vm2, vm2_state);
  digitalWrite(am2, am2_state);
  digitalWrite(vd2, vd2_state);
  digitalWrite(vmpd2, vmpd2_state);
  digitalWrite(vdpd2, vdpd2_state);
  
  delay(tempo_segundos * 1000);
}
<!--
**Gktesser/Gktesser** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
