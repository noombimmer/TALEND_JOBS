package routines;

import java.io.File;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.IOException;
import java.math.BigDecimal;
import java.math.MathContext;



/*
 * user specification: the function's comment should contain keys as follows: 1. write about the function's comment.but
 * it must be before the "{talendTypes}" key.
 * 
 * 2. {talendTypes} 's value must be talend Type, it is required . its value should be one of: String, char | Character,
 * long | Long, int | Integer, boolean | Boolean, byte | Byte, Date, double | Double, float | Float, Object, short |
 * Short
 * 
 * 3. {Category} define a category for the Function. it is required. its value is user-defined .
 * 
 * 4. {param} 's format is: {param} <type>[(<default value or closed list values>)] <name>[ : <comment>]
 * 
 * <type> 's value should be one of: string, int, list, double, object, boolean, long, char, date. <name>'s value is the
 * Function's parameter name. the {param} is optional. so if you the Function without the parameters. the {param} don't
 * added. you can have many parameters for the Function.
 * 
 * 5. {example} gives a example for the Function. it is optional.
 */
public class bms {

    /**
     * helloExample: not return value, only print "hello" + message.
     * 
     * 
     * {talendTypes} String
     * 
     * {Category} User Defined
     * 
     * {param} string("world") input: The string need to be printed.
     * 
     * {example} helloExemple("world") # hello world !.
     */
    public static void helloExample(String message) {
        if (message == null) {
            message = "World"; //$NON-NLS-1$
        }
        System.out.println("Hello " + message + " !"); //$NON-NLS-1$ //$NON-NLS-2$
    }
    public static BigDecimal getBDValue(Double value){
    	BigDecimal b = new BigDecimal(value,MathContext.DECIMAL64);
		return b;
    	
    }
    public static BigDecimal getBDValue(String value){
    	if (value != null || value.length() > 0) {
    		BigDecimal b = new BigDecimal(value);
    		return b;
    	}else{
    		BigDecimal b = new BigDecimal("0.000");
    		return b;
    	}
		
    	
    }    
    public static BigDecimal getDB_FC_Price(
    		Double qadPrice,
    		Double amisPrice,
    		String fc_type,
    		String month,
    		String fc_month,
    		String eq_month,
    		String fc_qad,
    		String eq_qad 
    		)
    {
    	if(fc_type.equals("Normal")){
//    		System.out.println("fc_type: " + fc_type 
//    				+ ", month: " + month
//    				+ ", fc_month: " + fc_month
//    				+ ", eq_month: " +eq_month
//    				+ ", qadPrice: " + String.valueOf(qadPrice)
//    				+ ", amisPrice: "+ String.valueOf(amisPrice)
//    				+ ", rst: " + String.valueOf(qadPrice)
//    				);
    		return getBDValue(qadPrice);
    	}else{
    		if(fc_type.equals("Forecast")){
    			if(getIntValue(month) >= getIntValue(fc_month)){
    				if(getIntValue(month) <= getIntValue(fc_qad)){
//    					System.out.println("fc_type: " + fc_type 
//        	    				+ ", month: " + month
//        	    				+ ", fc_month: " + fc_month
//        	    				+ ", eq_month: " +eq_month
//        	    				+ ", qadPrice: " + String.valueOf(qadPrice)
//        	    				+ ", amisPrice: "+ String.valueOf(amisPrice)
//        	    				+ ", rst: " + String.valueOf(qadPrice)
//        	    				);    				
        				return getBDValue(qadPrice);    					
    				}else{
//    					System.out.println("fc_type: " + fc_type 
//        	    				+ ", month: " + month
//        	    				+ ", fc_month: " + fc_month
//        	    				+ ", eq_month: " +eq_month
//        	    				+ ", qadPrice: " + String.valueOf(qadPrice)
//        	    				+ ", amisPrice: "+ String.valueOf(amisPrice)
//        	    				+ ", rst: " + String.valueOf(amisPrice)
//        	    				);    				
        				return getBDValue(amisPrice);
    				}
    				
    			}else{
//    				System.out.println("fc_type: " + fc_type 
//    	    				+ ", month: " + month
//    	    				+ ", fc_month: " + fc_month
//    	    				+ ", eq_month: " +eq_month
//    	    				+ ", qadPrice: " + String.valueOf(qadPrice)
//    	    				+ ", amisPrice: "+ String.valueOf(amisPrice)
//    	    				+ ", rst: " + String.valueOf(0.00)
//    	    				);
    				return getBDValue(0.00);
    			}
    		}else{
    			if(getIntValue(month) >= getIntValue(eq_month)){
    				if(getIntValue(month) <= getIntValue(eq_qad)){
//    					System.out.println("fc_type: " + fc_type 
//        	    				+ ", month: " + month
//        	    				+ ", fc_month: " + fc_month
//        	    				+ ", eq_month: " +eq_month
//        	    				+ ", qadPrice: " + String.valueOf(qadPrice)
//        	    				+ ", amisPrice: "+ String.valueOf(amisPrice)
//        	    				+ ", rst: " + String.valueOf(qadPrice)
//        	    				);
        				return getBDValue(qadPrice);
    				}else{
//    					System.out.println("fc_type: " + fc_type 
//        	    				+ ", month: " + month
//        	    				+ ", fc_month: " + fc_month
//        	    				+ ", eq_month: " +eq_month
//        	    				+ ", qadPrice: " + String.valueOf(qadPrice)
//        	    				+ ", amisPrice: "+ String.valueOf(amisPrice)
//        	    				+ ", rst: " + String.valueOf(amisPrice)
//        	    				);
        				return getBDValue(amisPrice);
    				}
    				
    			}else{
//    				System.out.println("fc_type: " + fc_type 
//    	    				+ ", month: " + month
//    	    				+ ", fc_month: " + fc_month
//    	    				+ ", eq_month: " +eq_month
//    	    				+ ", qadPrice: " + String.valueOf(qadPrice)
//    	    				+ ", amisPrice: "+ String.valueOf(amisPrice)
//    	    				+ ", rst: 0.00"
//    	    				);
    				return getBDValue(0.00);
    			}
    			
    		}
    		
    	}
    }
    public static String getDB_FC_DisplayFLG(
    		Double qadPrice,
    		Double amisPrice,
    		String fc_type,
    		String month,
    		String fc_month,
    		String eq_month,
    		String fc_qad,
    		String eq_qad 
    		)
    {
    	if(fc_type.equals("Normal")){
    		return "QAD";
    	}else{
    		if(fc_type.equals("Forecast")){
    			if(getIntValue(month) >= getIntValue(fc_month)){
    				if(getIntValue(month) <= getIntValue(fc_qad)){
        				return "QAD";    					
    				}else{
        				return "AMIS";
    				}
    				
    			}else{
    				return "NONE";
    			}
    		}else{
    			if(getIntValue(month) >= getIntValue(eq_month)){
    				if(getIntValue(month) <= getIntValue(eq_qad)){

        				return "QAD";
    				}else{
    					
        				return "AMIS";
    				}
    				
    			}else{
    				
    				return "NONE";
    			}
    			
    		}
    		
    	}
    }    
    
    public static Double getDecValue(String value){
    	Double b;
    	try {
    		b = new Double(value);
    	}catch(Exception e){
    		b = 0.00;
    	}
		return b;
    	
    }
    public static Integer getIntValue(String value){
    	Integer b;
    	try {
    		b = new Integer(value);
    	}catch(Exception e){
    		b = 0;
    	}
		return b;
    	
    }
    public static boolean checkFile(String fileName){
    	return (new File(fileName).exists());
    }
    public static String convertMonth2YearMonth(String MonthNumber,String yearNumber){
    	int nbr = 0;
    	String rtn = "";
    	String lYearNumber;
    	if(yearNumber.equals("cy")){
    		lYearNumber = TalendDate.getDate("yyyy");
    	}else{
    		lYearNumber = String.valueOf(Integer.parseInt(TalendDate.getDate("yyyy")) + 1 );
    	}
    	try{
    		nbr = Integer.parseInt(MonthNumber);
    	}catch(Exception e){
    		e.printStackTrace();
    	}
    	if(nbr < 10 ){
    		rtn = lYearNumber + "0" + String.valueOf(nbr);
    	}else{
    		rtn = lYearNumber + String.valueOf(nbr);
    	}
    	
    	return rtn;
    }
    public static BigDecimal selectPrice(BigDecimal qadPrice,BigDecimal amisPrice,String strCondition){
    	if(strCondition == null) {
    		return qadPrice;
    	}else{
	    	if(strCondition.equalsIgnoreCase("QAD")){
	    		return qadPrice;
	    	}else{
	    		return amisPrice;
	    	}
    	}
    	
    }
}
  