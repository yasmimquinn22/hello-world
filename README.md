# hello-world
import { StatusBar } from 'expo-status-bar';
import { StyleSheet, Button, View, ScrollView, TextInput,  Text, Alert} from 'react-native';;
import react,{useState} from 'react';
import { MaterialCommunityIcons } from '@expo/vector-icons';  

export default function App() {
  const [Cupom, setCupom] = useState('')
  const[ligar,setLigar]= useState(true);
  const clicarBotao = () => {
    setLigar(!ligar);
  }
  return (
    <View style={styles.container}>
      <ScrollView>
      <View>
      <Text style ={styles.titulo}>Molhos</Text>
      
      <View style={styles.bnt1}>
        <Button 
         title='Editar'       
         color={"#633F32"}
         onPress={() => Alert.alert('Aqui você escolhe o molho')}
        ></Button>

      </View>
      <Text></Text>
      
      <Text style={styles.molho1}> Tomate Tradicional </Text>       
      
      <View style={styles.checkmarcado}     >
        <MaterialCommunityIcons name="checkbox-marked" size={25} color="green" />
      
      </View>
      
      <Text style={styles.molho1}> Tomate light</Text>
      
      <View style={styles.checkvazio}>
        <MaterialCommunityIcons name="checkbox-blank-outline" size={25} color="black" />
      </View>
      
      <TextInput style={styles.imput}
      placeholder='Alguma observação ?'></TextInput>
      
      </View>

      <View>
      <Text style ={styles.titulo}>Queijos</Text>
      <View style={styles.bnt1}>
        <Button 
         title='Editar'       
         color={"#633F32"}
         onPress={() => Alert.alert('Aqui você escolhe o queijo')}
        ></Button>

      </View>
      <Text></Text>
      <Text style={styles.molho1}> Parmessão vegano </Text>       
      
      <View style={styles.checkmarcado}     >
        <MaterialCommunityIcons name="checkbox-marked" size={25} color="green" />
      
      </View>
      
      <Text style={styles.molho1}> Casca de caju</Text>
      
      <View style={styles.checkvazio}>
        <MaterialCommunityIcons name="checkbox-blank-outline" size={25} color="black" />
      </View>
      <Text style={styles.molho1}> Mussarela</Text>
      
      <View style={styles.checkvazio}>
        <MaterialCommunityIcons name="checkbox-blank-outline" size={25} color="black" />
      </View>
      
      <TextInput style={styles.imput}
      placeholder='Alguma observação ?'></TextInput>
      
      </View>
      <View>
      <Text style ={styles.titulo}>Recheios</Text>
      <View style={styles.bnt1}>
        <Button 
         title='Editar'       
         color={"#633F32"}
         onPress={() => Alert.alert('Aqui você escolhe os recheios')}
        ></Button>

      </View>
      <Text></Text>
      <Text style={styles.molho1}> Palmito </Text>       
      
      <View style={styles.checkmarcado}     >
        <MaterialCommunityIcons name="checkbox-marked" size={25} color="green" />
      
      </View>
      
      <Text style={styles.molho1}> Casca de caju</Text>
      
      <View style={styles.checkvazio}>
        <MaterialCommunityIcons name="checkbox-blank-outline" size={25} color="black" />
      </View>
      <Text style={styles.molho1}> Abacaxi</Text>
      
      <View style={styles.checkvazio}>
        <MaterialCommunityIcons name="checkbox-blank-outline" size={25} color="black" />
      </View>
      
      <TextInput style={styles.imput}
      placeholder='Alguma observação ?'></TextInput>
      
      </View>
      <Text></Text>

      <Button title='Cupom ? aperte aqui !!!'       
         color={"#633F32"}
        onPress={clicarBotao} ></Button>
      <Text></Text>
      {
        ligar ?
        <Text></Text>
        :

      <TextInput style={styles.imput}
      placeholder='Digite seu cupom'
      onChangeText={setCupom}></TextInput>

      }

      <Text style={styles.cupomtxt}> {Cupom} </Text>

      <TextInput style={styles.imput}
       placeholder='Quantas você vai querer ?'
      keyboardType='numeric'></TextInput>
      <Text></Text>


      <Button title='Enviar'       
         color={"#633F32"}
         onPress={() => Alert.alert('Seu pedido foi enviado')}></Button>
         <Text></Text>
      </ScrollView>
      <StatusBar style="auto" />
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#028D3D', 
  },
  titulo:{    
    marginTop:20,
    fontSize:40,
    textAlign:"center",     
    color:"#fff" ,  
  },
  btn1:{
    flex:2,
    justifyContent:"flex-end",
    alignItems:"right",
     width:250,  
  
    
  },
  molho1:{
    textAlign:"center",
    textAlignVertical:"center",
    fontSize:20,
    backgroundColor:"#fff",
    height:50,
    width:250,       
  },
  checkmarcado:{
     textAlign:"center",
    flexDirection:"row",
    justifyContent:"flex-end",
    backgroundColor:"#006400",
    marginLeft:385,
    top:-35
  },
  checkvazio:{
     textAlign:"left" ,
    flexDirection:"row",
    justifyContent:"flex-end" ,
    backgroundColor:"#006400",
    marginLeft:385,
    top:-35

  },
  imput:{
     borderWidth:1,
     height:50,
     width:250, 
    fontSize:20,
    backgroundColor:"#fff"
  },
  cupomtxt:{
    fontSize:30
  }


});
