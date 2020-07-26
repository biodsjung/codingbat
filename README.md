# codingbat- map2 allswap()
public String[] allSwap(String[] strings) {

  Map <String, Integer> map = new HashMap();
  
  String firstChar= "";
 
  
  for (int i=0; i< strings.length; i++) {
     
     firstChar = strings[i].substring(0,1);
  
  if(map.containsKey(firstChar) ) {
    String temp = strings[map.get(firstChar)] ;
    strings[map.get(firstChar)]= strings[i];
    strings[i] = temp;
    
    map.remove(firstChar);
  }
  else map.put(firstChar, i);
  }
  
  return strings;
}
