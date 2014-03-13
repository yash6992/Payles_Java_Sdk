Payles_Java_Sdk
===============
Sign up for a Payles account here to get the Payles user key for the next steps.
1.	Download the java library from here.

2.	Import the java file into your existing Java project by copying it in your Java project 	folder and adding it to your project’s build path. 
	You can also alternatively add it as an external jar file to your project.

3.	Add the following import statements to your Class:
	import com.payles.PaylesAPI;
	import com.payles.Medicine;

To use the API in your Java Class, you need to add your key which you have received and then follow these steps.

4. 	Add your Payles key as:
	PaylesAPI.key="yash6992";

5. 	You can use the following method to get an list of all the brand names  suggestions for 	the parameter search String (find)
	return type:  ArrayList<String>
	ArrayList<String> 	medicineSuggestions=PaylesAPI.getMedicineSuggestions(find);


6. 	You can use the following method which will give details for the medicine whose 	brand name is parameter String (brand).
	return type: Medicine
	This Object has getter methods for its various variables as follows.
	Medicine medicine= PaylesAPI.getMedicineData(brand);
	Its variable can be accessed as:
	medicine.getManufacturer());
	medicine.getBrand());
	medicine.getCategory());
	medicine.getDClass());
	medicine.getUnitType());
	medicine.getUnitQty());
	medicine.getPackageType());
	medicine.getPackageQty());
	medicine.getPackagePrice());
	medicine.getUnitPrice());
	medicine.getGenericId());

7.	You can use the following method which will give you all alternatives for any medicine 	whose brand name is the parameter String(brand).
	return type: HashMap<String, Medicine>
	The function can be accesses as:
	HashMap<String, Medicine> medicineAlternatives= 		      	                      PaylesAPI.getMedicineAlternatives(brand2);
	
	The HashMap key is the drugs' brand name.
	The Medicine List can be accessed as:

	for (String alternateBrand: medicineAlternatives.keySet()){
		   ..
		   ..
           Medicine alternateMedicine = 				   			                 medicineAlternatives.get(alternateBrand);  
               ..
		   ..
          }
