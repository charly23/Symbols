Symbols
=======
<?php
if( !class_exists( 'SYMBOLS' ) ){
    
    class SYMBOLS{
        
        public static function crcle_row(){
            $points = "*";
            $count_max = 10; 
            for($ix=0;$ix<=$count_max;$ix++){
                if( intval($ix) AND is_string($points)){
                    $i1_array[] = $points;
                    $i2_array[] = $points;
                    if( intval($ix) AND $ix >= 1 AND $ix <=5 ){
                       $i3_array[] = $points;
                    }
                }
            }
            
            if( is_array( $i1_array)){
                foreach( $i1_array as $i1_array_row => $i1_array_var){
                    if(!empty( $i1_array_var)){
                         echo $i1_array_var;
                    }
                }
            }
            
            if( is_array( $i3_array)){
                $dal = ".";
                $count = 16;
                $ic_value = null;
                for($ic=0; $ic<=$count; $ic++){
                    if( intval($ic) AND is_string($dal)){
                        $ic_value .= $dal;
                    }
                }
                foreach( $i3_array as $i3_array_row => $i3_array_var){
                    if(!empty( $i3_array_var)){
                         echo "<br/>" . $i3_array_var . $ic_value . $i3_array_var;
                    }
                }
            }
            
            if( is_array( $i2_array)){
                echo '<br/>';
                foreach( $i2_array as $i2_array_row => $i2_array_var ){
                    if(!empty( $i2_array_var)){
                         echo $i2_array_var;
                    }
                }
            }   
        }
        
        public static function triangle_top($string=null){
            $dal = ".";
            if( !is_null( $string)){
                $count = 21;
                for($i=0; $i<=$count; $i++){
                     if( intval($i)){
                          if( $i >= 11 AND $i <= 11 ){
                              echo $string;
                          } else {
                              echo $dal;
                          }
                     }
                }
            }
        }
        
        public static function triangle_center($string=null){
            $dal = ".";
            if( !is_null( $string)){
                
                 $d_number = array( 8, 7, 6, 5, 4 );
                 
                 // 1
                 $center_point1 = "..";
                 $id1_result = null;
                 echo '<br/>';
                 for($id1=0; $id1<=$d_number[0]; $id1++){
                    if( intval( $id1 )){
                        $id1_result .= $dal;
                    }
                 }
                 echo $id1_result . $string . $center_point1 . $string . $id1_result;
                 
                 // 2
                 $center_point2 = "....";
                 $id2_result = null;
                 echo '<br/>';
                 for($id2=0; $id2<=$d_number[1]; $id2++){
                    if( intval( $id2 )){
                        $id2_result .= $dal;
                    }
                 }
                 echo $id2_result . $string . $center_point2 . $string . $id2_result;
                 
                 // 3 
                 $center_point3 ="......";
                 $id3_result = null;
                 echo '<br/>';
                 for($id3=0; $id3<=$d_number[2]; $id3++){
                    if( intval( $id3 )){
                        $id3_result .= $dal;
                    }
                 }
                 echo $id3_result . $string . $center_point3 . $string . $id3_result;
                 
                 // 4         
                 $center_point4 ="........";
                 $id4_result = null;
                 echo '<br/>';
                 for($id4=0; $id4<=$d_number[3]; $id4++){
                    if( intval( $id4 )){
                        $id4_result .= $dal;
                    }
                 }
                 echo $id4_result . $string . $center_point4 . $string . $id4_result;
                 
                 // 5
                 $center_point5 ="..........";
                 $id5_result = null;
                 echo '<br/>';
                 for($id5=0; $id5<=$d_number[4]; $id5++){
                    if( intval( $id5 )){
                        $id5_result .= $dal;
                    }
                 }
                 echo $id5_result . $string . $center_point5 . $string . $id5_result;
            }
        }
        
        public static function triangle_bottom($string=null){
            if( !is_null( $string)){
                 echo '<br/>';
                 $side_point = "...";
                 $count_bottom = 8;
                 $bottom_result = null;
                 for($cix=0; $cix<=$count_bottom; $cix++){
                     if( intval($cix)){
                          $bottom_result .= $string; 
                     }
                 }
                 echo  $side_point . $bottom_result . $side_point;
            } 
        }
        
        public static function triangle_row(){
            $points = "*";
            self::triangle_top($points);
            self::triangle_center($points);
            self::triangle_bottom($points);
        }
    }
}
?>

<div class="cryle"><?php echo SYMBOLS::crcle_row(); ?></div>
<div class="triangle"><?php echo SYMBOLS::triangle_row(); ?></div>
