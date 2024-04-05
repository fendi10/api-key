 //script php
        $data = [
        'api_key' => '4a687f91e871033f315c7802755b35c89cf3b106',
        'sender' => '082286843278',
        'number' => '081277878884',
        'message' => 'Pesan yang di kirim'
              ];
           $curl = curl_init();
                                                    
             curl_setopt_array($curl, array(
              CURLOPT_URL => 'https://wa.srv33.wapanels.com/send-message',
              CURLOPT_RETURNTRANSFER => true,
              CURLOPT_ENCODING => '',
              CURLOPT_MAXREDIRS => 10,
              CURLOPT_TIMEOUT => 0,
              CURLOPT_FOLLOWLOCATION => true,
              CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
              CURLOPT_CUSTOMREQUEST => 'POST',
              CURLOPT_POSTFIELDS => json_encode($data),
              CURLOPT_HTTPHEADER => array(
              'Content-Type: application/json'
              ),
              ));
                                                    
              $response = curl_exec($curl);
                                                    
              curl_close($curl);
              echo $response;
