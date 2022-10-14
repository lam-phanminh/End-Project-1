pipeline{
    // tools{
    //     jdk 'myjava'
    //     maven 'mvnn'
    // }
	agent {label 'kslave1'}
	// agent any
        stages{
            stage('Checkout'){	    
                steps{
		            echo 'cloning..'
                    git 'https://github.com/lam-phanminh/End-Project-1.git'
                }
            }
            stage('Build......'){	    
                steps{
		            sh 'docker build -t phanminhlam/php-app:$BUILD_NUMBER'
                }
            }
            stage('Docker login && push image ......'){	    
                steps{
		            sh 'docker login -u phanminhlam -p Phanminhlam1@ && docker push phanminhlam/myimage:$BUILD_NUMBER'
                }
            }
            // stage('Deploy...'){	    
            //     steps{
		    //         sh 'docker login -u phanminhlam -p Phanminhlam1@ && docker push phanminhlam/myimage:$BUILD_NUMBER'
            //     }
            // }        
     
        }
}
