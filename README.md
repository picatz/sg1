# SG1

```
                                                _______                                
                                        _,.--==###\_/=###=-.._                         
                                    ..-'     _.--\\_//---.    `-..                     
                                 ./'    ,--''     \_/     `---.   `\.                  
                               ./ \ .,-'      _,,......__      `-. / \.                
                             /`. ./\'    _,.--'':_:'"`:'`-..._    /\. .'\              
                            /  .'`./   ,-':":._.:":._.:"+._.:`:.  \.'`.  `.            
                          ,'  //    .-''"`:_:'"`:_:'"`:_:'"`:_:'`.     \   \           
                         /   ,'    /'":._.:":._.:":._.:":._.:":._.`.    `.  \          
                        /   /    ,'`:_:'"`:_:'"`:_:'"`:_:'"`:_:'"`:_\     \  \         
                       ,\\ ;     /_.:":._.:":._.:":._.:":._.:":._.:":\     ://,        
                       / \\     /'"`:_:'"`:_:'"`:_:'"`:_:'"`:_:'"`:_:'\    // \.       
                      |//_ \   ':._.:":._.+":._.:":._.:":._.:":._.:":._\  / _\\ \      
                     /___../  /_:'"`:_:'"`:_:'"`:_:'"`:_:'"`:_:'"`:_:'"'. \..__ |      
                      |  |    '":._.:":._.:":._.:":._.:":._.:":._.:":._.|    |  |      
                      |  |    |-:'"`:_:'"`:_:'"`:_:'"`:_:'"`:_:'"`:_:'"`|    |  |      
                      |  |    |":._.:":._.:":._.:":._.:":._.+":._.:":._.|    |  |      
                      |  :    |_:'"`:_:'"`:_+'"`:_:'"`:_:'"`:_:'"`:_:'"`|    ; |       
                      |   \   \.:._.:":._.:":._.:":._.:":._.:":._.:":._|    /  |       
                       \   :   \:'"`:_:'"`:_:'"`:_:'"`:_:'"`:_:'"`:_:'.'   ;  |        
                        \  :    \._.:":._.:":._.:":._.:":._.:":._.:":,'    ;  /        
                        `.  \    \..--:'"`:_:'"`:_:'"`:_:'"`:_:'"`-../    /  /         
                         `__.`.'' _..+'._.:":._.:":._.:":._.:":.`+._  `-,:__`          
                      .-''    _ -' .'| _________________________ |`.`-.     `-.._      
                _____'   _..-|| :.' .+/;;';`;`;;:`)+(':;;';',`\;\|. `,'|`-.      `_____
                  MJP .-'   .'.'  :- ,'/,',','/ /./|\.\ \`,`,-,`.`. : `||-.`-._        
                          .' ||.-' ,','/,' / / / + : + \ \ \ `,\ \ `.`-||  `.  `-.     
                       .-'   |'  _','<', ,' / / // | \\ \ \ `, ,`.`. `. `.   `-.       
                                                   :              - `. `.              
                                            BECAUSE
                                                   REASONS      
```

SG1 is a wanna be swiss army knife for data encryption, exfiltration and covert communication. In its core SG1 aims to be as simple to use as netcat while maintaining high modularity.

**WORK IN PROGRESS, DON'T JUDGE**

## Installation

    go get github.com/miekg/dns
    go get github.com/evilsocket/sg1

    cd $GOPATH/src/github.com/evilsocket/sg1/
    make

## Contribute

You can contribute by:

1) Grep for `TODO` and see how you can help.
2) Implement a new module ( see `modules/raw.go` for very basic example or `modules/aes.go` for complete one ).
3) Implement a new channel ( see `channels/*.go` ).

## Examples

Simple file exfiltration over DNS:
![file](https://pbs.twimg.com/media/DPH8KkAWsAE5rZZ.jpg:large)

Quick and dirty AES encrypted chat over TCP:
![aes-tcp](https://pbs.twimg.com/media/DPHAlOXWAAA9kKv.jpg:large)

Encrypting data in AES and exfiltrate it via DNS requests:
![aes-dns](https://pbs.twimg.com/media/DPHsSLwWkAEbg7P.jpg:large)

Test with different operating systems ( tnx to [decoded](https://twitter.com/d3d0c3d) ):
![freebsd](https://pbs.twimg.com/media/DPH0612UQAA3gzg.jpg:large)

With bouncing to another host:
![bounce](https://pbs.twimg.com/media/DPHtBocWsAAyDVN.jpg:large)

Just use `sg1 -h` to see a list of available channels and modules, try to pipe them and see what happens, you can also transfer files and make requests "bounce" to several machines with random AES keys ^_^

## License

SG1 was made with ♥  by [Simone Margaritelli](https://www.evilsocket.net/) and it's released under the GPL 3 license.

