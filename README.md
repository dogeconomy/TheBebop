# TheBebop
A means of hosting data over the web offering potentially less security risk and adding more anonymity. Protecting your data, identity, etc.. and the people that host it from bad actors.
------------------------------------
Idea Board / Overall Goal Board
------------------------------------
[Please use raw link for proper formatting]
https://raw.githubusercontent.com/dogeconomy/TheBebop/main/README.md


// Create server which can host https on 443 and http on 80

// Bebop will host files served via ipfs in a webserver fashion
// offering a bit more security for everyone. (hopefully)
// 
// Bebop will need to scan the appointed "web hosting directory"
// (ex: /var/www/ or /etc/httpdocs or where ever) and add each one of the files
// into ipfs and retreive an address for the files location.
// 
// Bebop will also need to first verify the files and then place them into 
// a separate container "folder" of users choice.
//
// Bebop will then need to:
// - Add a file, 
// -- Then store the files ipfs data: address or whatever else needed.
//    ex: 
//       address: QmVnf8FZ4pQGyWtyMYZPWecdxhjUZsebDegHqZJuuAM7kS
//       filename: GoLang Tutorial Notes
//       extension: .txt
//       password: (optional) | **for encrypted data types**
//       thought: attach creator md5 to double verify / extra security layer?  
// 
// --- An additional encryption layer could happen before transmission as well
//     so that the data is first encrypted during the adding proccess to ipfs,  
//     the key being stored in some json format on ipfs as well.
//
// ---- Once the files are uploaded to IPFS the original content can be taken
//      off of the "Client Web Files" area so no hard data is stored on the server.
//
// ---- There would need to be a way for Bebop to identify changes within files upon new scans
//      when files are added, so that the users are never obtaining old information.
// ------- Once new files are submitted and a scan is made Bebop should confirm any data that is 
//         not matching old ipfs addresses to confirm the resource update.
//
//                                             _____[U/L]_____
//     -------------------------               | add file to |
//     |   [Bebop Webserver]   |          _____|    ipfs     |----|------------------------------|
//     ------------------------|         |     |_____^_______|    |                              |
//                            |_________|_________  |   =========|==================             |
//                            | Client Web Files | U/L //  if no encryption skip   \\            |
//                            |_(recursive scan__|--|--\\    to storing to ipfs     \\           |
//                                                  |   \\===========================\\          |
//                                                  |                                 \\         |
//                                |   ======================        |=====================| (or) |---------------------------|
//                                |   |[Encryption Process]|  --->  | Store Data to IPFS  | ---> | Store as encrypted object |
//                                |   ======(optional)======        |   (non encrypted!)  | (if) | encrypted                 |
//                                |         ^(maybe?)^              ===========||==========      |----------------|----------|
//                                |             ||                -------------\/---------              ||   _____|__________|______________________
//                                |------------//\\--------------|[ | Create a data index:]|            ||  | So encrypt the data and then add the |
//                                              || (if encrypted)|[ |  address,filename,  ]|            \/  |        encrypted data to IPFS        |
//                                              ||     <-- <-----|[-| filetype, password, ]|____________||  |--------------------------------------|
//                                              | (option chosen)|[   directory/location, ]|_____________|  
//                                              |----------------|[   creator md5 maybe?  ]|                
//                                                             --------------||-----------                
//              |------------------|                                         ||                           
//              |    IPFSWWW Dir   |                           |=============\/============|              
//              |------------------|                           | Store into IPFS Database! |
//              |                  |                           |---------------------------|
//              |                  |                           | IPFS database will work   |
//              |                  |                           | how it sounds, a database |
//              |__________________|                           | which works off of the    |
//                                                             | IPFS network, storing and |
//                                                             | retrieving data           |
//                                                             |-------------||------------|
//                                                                           || 
//                                                                           || 
//                                                             |-------------\/----------------|
//                                                             | todo todo                     |__
//                                                             |---------------------------------|
//                                                             | lorum ipsum, still a thought    |
//                                                <-- <-- <--  | in progress, this is just some  |
//                                                             | useless text to fill up my cool |
//                                                             | asii text box I spent entirely  |
//                                                             | too much time on!               |
//                                                             | --------------------------------|
// 
// 
// Create ipfs webserver on port 80
//
// Create ipfs webserver on port 443

