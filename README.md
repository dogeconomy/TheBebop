// These are some ideas/goals jotted down by myself in hopes to create a better internet for tomorrow! <br>
// For best viewing and proper format, please view the **RAW** format here: <br>
// https://raw.githubusercontent.com/dogeconomy/TheBebop/main/README.md <br>
//<br>
// Please feel free to comment and contribute any thoughts, ideas, etc.. this may have spawned. <br>
// Always down to listen to new ideas and perspectives. <br>
// <br>
// Create server which can host https on 443 and http on 80 <br>
<br>
// Bebop will host files served via ipfs in a webserver fashion <br>
// offering a bit more security for everyone. (hopefully) <br>
// <br>
// Bebop will need to scan the appointed "web hosting directory"<br>
// (ex: /var/www/ or /etc/httpdocs or where ever) and add each one of the files <br>
// into ipfs and retreive an address for the files location.<br>
//  <br>
// Bebop will also need to first verify the files and then place them into <br>
// a separate container "folder" of users choice.<br>
// <br>
// Bebop will then need to: <br>
// - Add a file, <br>
// -- Then store the files ipfs data: address or whatever else needed. <br>
//    ex: <br>
//       address: QmVnf8FZ4pQGyWtyMYZPWecdxhjUZsebDegHqZJuuAM7kS <br>
//       filename: GoLang Tutorial Notes <br>
//       extension: .txt <br>
//       password: (optional) | **for encrypted data types** <br>
//       thought: attach creator md5 to double verify / extra security layer? <br>
//  <br>
// --- An additional encryption layer could happen before transmission as well <br>
//     so that the data is first encrypted during the adding proccess to ipfs,  <br>
//     the key being stored in some json format on ipfs as well. <br>
// <br>
// ---- Once the files are uploaded to IPFS the original content can be taken <br>
//      off of the "Client Web Files" area so no hard data is stored on the server. <br>
// <br>
// ------ Alternatively, ipfs should not be the only means of data storage. <br>
//        If a system where you could utilize multiple services in a hybrid <br>
//        fashion could allow for effective data storage then this is an option <br>
//        I would like to explore for Bebop! <br>
// <br>
//                                             _____[U/L]_____ <br>
//     -------------------------               | add file to | <br>
//     |   [Bebop Webserver]   |          _____|    ipfs     |----|-------------------------------| <br>
//     ------------------------|         |     |_____^_______|    |                               | <br>
//                             |_________|_________  |   =========|==================             | <br>
//                             | Client Web Files | U/L //  if no encryption skip   \\            | <br>
//                             |_(recursive scan__|--|--\\    to storing to ipfs     \\           | <br>
//                                                   |   \\  (will hold enc anyway)   \\          | <br>
//                                                   |    \\===========================\\         | <br>
//                                                   |                                            | <br>
//                                                   |   ======================        |=====================| (or) |---------------------------| <br>
//                                                   |   |[Encryption Process]|  --->  | Store Data to IPFS  | ---> | Store as encrypted object | <br>
//                                                   |   ======(optional)======        |   (non encrypted!)  | (if) | encrypted                 | <br>
//                                                   |         ^(maybe?)^              ===========||==========      |----------------|----------| <br>
//                                                   |             ||                -------------\/---------              ||   _____|__________|______________________ <br>
//                                                   |------------//\\--------------|[ | Create a data index:]|            ||  | So encrypt the data and then add the | <br>
//                                                                 || (if encrypted)|[ |  address,filename,  ]|            \/  |        encrypted data to IPFS        | <br>
//                                                                 ||     <-- <-----|[-| filetype, password, ]|____________||  |--------------------------------------| <br>
//                                                                 | (option chosen)|[   directory/location, ]|_____________|   <br>
//                                                                 |----------------|[   creator md5 maybe?  ]|                 <br>
//                                                                                  --------------||-----------                 <br>
//                                   |------------------|                                         ||                            <br>
//                                   |    IPFSWWW Dir   |                           |=============\/============|               <br>
//                                   |------------------|                           | Store into IPFS Database! |               <br>
//                                   |                  |                           |---------------------------|               <br>
//                                   |                  |                           | IPFS database will work   |  <br>
//                                   |                  |                           | how it sounds, a database | <br>
//                                   |__________________|                           | which works off of the    | <br>
//                                                                                  | IPFS network, storing and | <br>
//                                                                                  | retrieving data           | <br>
//                                                                                  |-------------||------------| <br>
//                                                                                                ||  <br>
//                                                                                                ||  <br>
//                                                                                  |-------------\/----------------|  <br>
//                                                                                  | todo todo                     |__ <br>
//                                                                                  |---------------------------------| <br>
//                                                                                  | lorum ipsum, still a thought    | <br>
//                                                                     <-- <-- <--  | in progress, this is just some  | <br>
//                                                                                  | useless text to fill up my cool | <br>
//                                                                                  | asii text box I spent entirely  | <br>
//                                                                                  | too much time on!               | <br>
//                                                                                  | --------------------------------| <br>
// Create ipfs webserver on port 80 <br>
//  <br>
// Create ipfs webserver on port 443 <br>

