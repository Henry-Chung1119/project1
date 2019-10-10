#include <iostream>
#include <fstream>
#include <cstring>
using namespace std;
class block{
    public:
        int row,col;
        int **shape;
        block():row(0),col(0){}
        block(int row,int col):row(row),col(col){}

};
class T1:public block{
    public:
        //int **shape;
        T1():block(2,3){
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[0][1]=1;
            shape[0][2]=1;
            shape[1][0]=0;
            shape[1][1]=1;
            shape[1][2]=0;
        };
        ~T1(){
            for(int i=0;i<row;i++)
                delete[] shape[i];
            delete[] shape;
        };
};
class T2:public block{
    public:
        //int **shape;
        T2(){
            row=3;
            col=2;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=0;
            shape[0][1]=1;
            shape[1][0]=1;
            shape[1][1]=1;
            shape[2][0]=0;
            shape[2][1]=1;
        };
};

class T3:public block{
    public:
        T3(){
            row=2;
            col=3;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=0;
            shape[0][1]=1;
            shape[0][2]=0;
            shape[1][0]=1;
            shape[1][1]=1;
            shape[1][2]=1;
        };
};

class T4:public block{
    public:
        T4(){
            row=3;
            col=2;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[0][1]=0;
            shape[1][0]=1;
            shape[1][1]=1;
            shape[2][0]=1;
            shape[2][1]=0;
        };
};

class L1:public block{
    public:
        L1(){
            row=3;
            col=2;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[0][1]=0;
            shape[1][0]=1;
            shape[1][1]=0;
            shape[2][0]=1;
            shape[2][1]=1;
        };
};

class L2:public block{
    public:
        L2(){
            row=2;
            col=3;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[0][1]=1;
            shape[0][2]=1;
            shape[1][0]=1;
            shape[1][1]=0;
            shape[1][2]=0;
        };
};

class L3:public block{
    public:
        L3(){
            row=3;
            col=2;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[0][1]=1;
            shape[1][0]=0;
            shape[1][1]=1;
            shape[2][0]=0;
            shape[2][1]=1;
        };
};

class L4:public block{
    public:
        L4(){
            row=2;
            col=3;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=0;
            shape[0][1]=0;
            shape[0][2]=1;
            shape[1][0]=1;
            shape[1][1]=1;
            shape[1][2]=1;
        };
};

class J1:public block{
    public:
        J1(){
            row=3;
            col=2;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=0;
            shape[0][1]=1;
            shape[1][0]=0;
            shape[1][1]=1;
            shape[2][0]=1;
            shape[2][1]=1;
        };
};

class J2:public block{
    public:
        J2(){
            row=2;
            col=3;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[0][1]=0;
            shape[0][2]=0;
            shape[1][0]=1;
            shape[1][1]=1;
            shape[1][2]=1;
        };
};

class J3:public block{
    public:
        J3(){
            row=3;
            col=2;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[0][1]=1;
            shape[1][0]=1;
            shape[1][1]=0;
            shape[2][0]=1;
            shape[2][1]=0;
        };
};

class J4:public block{
    public:
        J4(){
            row=2;
            col=3;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[0][1]=1;
            shape[0][2]=1;
            shape[1][0]=0;
            shape[1][1]=0;
            shape[1][2]=1;
        };
};

class S1:public block{
    public:
        S1(){
            row=2;
            col=3;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=0;
            shape[0][1]=1;
            shape[0][2]=1;
            shape[1][0]=1;
            shape[1][1]=1;
            shape[1][2]=0;
        };
};

class S2:public block{
    public:
        S2(){
            row=3;
            col=2;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[0][1]=0;
            shape[1][0]=1;
            shape[1][1]=1;
            shape[2][0]=0;
            shape[2][1]=1;
        };
};

class Z1:public block{
    public:
        Z1(){
            row=2;
            col=3;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[0][1]=1;
            shape[0][2]=0;
            shape[1][0]=0;
            shape[1][1]=1;
            shape[1][2]=1;
        };
};

class Z2:public block{
    public:
        Z2(){
            row=3;
            col=2;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=0;
            shape[0][1]=1;
            shape[1][0]=1;
            shape[1][1]=1;
            shape[2][0]=1;
            shape[2][1]=0;
        };
};

class I1:public block{
    public:
        I1(){
            row=4;
            col=1;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[1][0]=1;
            shape[2][0]=1;
            shape[3][0]=1;
        };
};

class I2:public block{
    public:
        I2(){
            row=1;
            col=4;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[0][1]=1;
            shape[0][2]=1;
            shape[0][3]=1;
        };
};

class O:public block{
    public:
        O(){
            row=2;
            col=2;
            shape=new int*[row];
            for(int i=0;i<row;i++)
                shape[i]=new int[col];
            shape[0][0]=1;
            shape[0][1]=1;
            shape[1][0]=1;
            shape[1][1]=1;
        };
};
//2*3 block
template<class T>
void TetrisBattle23(T &fallingblock, int **matrix, int index, int matrixrow, int matrixcol, bool &endgame){
    bool check=0;
    bool stop=0;
    bool end=0;
    int eliminationtimes=0;
    int eliminationlocation=0;
    int stopfalling=0;
    //T1 fallingblock;
    for(int fallingtimes=0;fallingtimes<=matrixrow;fallingtimes++){
        //if(matrix[fallingtimes+3][col])
        for(int j=index-1;j<index+fallingblock.col-1;j++){
            if(matrix[fallingtimes+2][j]==1){
                if(matrix[fallingtimes+3][j]==1){
                    if(fallingtimes==1){
                        endgame=1;
                        //stop=1;
                        //end=1;
                        break;
                    }
                    else{
                        stop=1;
                        stopfalling=fallingtimes-1;
                    //cout << "yes" << endl;
                        break;
                    }
                }
            }
        }
        if(endgame)
            break;
        if(!stop){
            for(int col=index-1;col<index-1+fallingblock.col;col++){
                if(fallingtimes==0){
                    matrix[fallingtimes+3][col]=fallingblock.shape[1][col-index+1];
                    matrix[fallingtimes+2][col]=fallingblock.shape[0][col-index+1];
                }
                else if(matrix[fallingtimes+2][col]==0 && matrix[fallingtimes+3][col]==1){
                    matrix[fallingtimes+2][col]=matrix[fallingtimes+1][col];
                    matrix[fallingtimes+1][col]=0;
                    stop=1;
                    stopfalling=fallingtimes;
                    //cout << "yes right" << endl;
                }
                else{
                    if(fallingtimes==matrixrow){
                        stop=1;
                        stopfalling=fallingtimes;
                    }
                    matrix[fallingtimes+3][col]=matrix[fallingtimes+2][col];
                    matrix[fallingtimes+2][col]=matrix[fallingtimes+1][col];
                    matrix[fallingtimes+1][col]=0;
                }
            }
        }
        if(stop){
            for(int elimination=1;elimination<=fallingblock.row;elimination++){
                for(int col=0;col<matrixcol;col++){
                    if(matrix[stopfalling+elimination+1][col]==0){
                        check=0;
                        //end=1;
                        //cout << "yes again" << endl;
                        break;
                    }
                    else
                        check=1;
                }
                if(check){
                    for(int col=0;col<matrixcol;col++){
                        matrix[stopfalling+elimination+1][col]=0;
                    }
                    //check=0;
                    eliminationlocation=elimination;
                    eliminationtimes++;
                }
            }
        }
        if(eliminationtimes>0){
            switch(eliminationtimes){
                case(0):
                    end=1;
                    break;
                case(1):
                    //different for every function
                    for(int row=stopfalling+eliminationlocation+1;row>0;row--){
                        for(int col=0;col<matrixcol;col++){
                            matrix[row][col]=matrix[row-1][col];
                        }
                    }
                    for(int col=0;col<matrixcol;col++){
                        matrix[0][col]=0;
                    }
                    end=1;
                    break;
                case(2):
                    //different for every function
                    for(int row=stopfalling+eliminationlocation+1;row>1;row--){
                        for(int col=0;col<matrixcol;col++){
                            matrix[row][col]=matrix[row-2][col];
                        }
                    }
                    for(int col=0;col<matrixcol;col++){
                        matrix[0][col]=0;
                        matrix[1][col]=0;
                    }
                    end=1;
                    break;
                default:
                    cout << "Eliminationtimes error!" << endl;
                    end=1;
                    break;
            }
        }
        //stop=0;
        //end=1;
        //cout << "Falling:" << fallingtimes << endl;
        if(end)
            break;
        /*cout << "Falling:" << fallingtimes << endl;
        for(int i=0;i<matrixrow+5;i++){
            for(int j=0;j<matrixcol;j++){
                cout << matrix[i][j];
            }
        cout << endl;
        }*/
    }
}



//3*2 block
template<class T>
void TetrisBattle32(T &fallingblock, int **matrix, int index, int matrixrow, int matrixcol, bool &endgame){
    bool check=0;
    bool stop=0;
    bool end=0;
    int eliminationtimes=0;
    int eliminationlocation=0;
    int stopfalling=0;
    //T1 fallingblock;
    for(int fallingtimes=0;fallingtimes<=matrixrow;fallingtimes++){
        //if(matrix[fallingtimes+3][col])
        for(int j=index-1;j<index+fallingblock.col-1;j++){
            if(fallingblock.shape[1][j-index+1]==0 && fallingblock.shape[2][j-index+1]==0){
                if(matrix[fallingtimes+1][j]==1){
                    if(matrix[fallingtimes+2][j]==1){
                        if(matrix[fallingtimes+3][j]==1){
                                stop=1;
                                stopfalling=fallingtimes-1;
                                //fallingtimes=fallingtimes-1;
                                break;
                        }
                    }
                }
            }
            else{
                if(matrix[fallingtimes+2][j]==1){
                    if(matrix[fallingtimes+3][j]==1){
                        if(fallingtimes==1){
                            endgame=1;
                            //stop=1;
                            //end=1;
                            break;
                        }
                        else{
                            stop=1;
                            stopfalling=fallingtimes-1;
                            //fallingtimes=fallingtimes-1;
                            //cout << "yes" << endl;
                            break;
                        }
                    }
                }
            }
        }

        if(endgame)
            break;
        //different for every function------
        if(!stop){
            for(int col=index-1;col<index-1+fallingblock.col;col++){
                if(fallingtimes==0){
                    matrix[fallingtimes+3][col]=fallingblock.shape[2][col-index+1];
                    matrix[fallingtimes+2][col]=fallingblock.shape[1][col-index+1];
                    matrix[fallingtimes+1][col]=fallingblock.shape[0][col-index+1];
                }
                else if(matrix[fallingtimes+2][col]==0 && matrix[fallingtimes+3][col]==1){
                    if(matrix[fallingtimes+1][col]==1){
                        stop=1;
                        stopfalling=fallingtimes;
                    }
                    matrix[fallingtimes+2][col]=matrix[fallingtimes+1][col];
                    matrix[fallingtimes+1][col]=matrix[fallingtimes][col];
                    matrix[fallingtimes][col]=0;

                    //cout << "yes right" << endl;
                }
                else if(matrix[fallingtimes+1][col]==0 && matrix[fallingtimes+2][col]==1 && matrix[fallingtimes+3][col]==1){
                    matrix[fallingtimes+1][col]=matrix[fallingtimes][col];
                    matrix[fallingtimes][col]=0;
                    stop=1;
                    stopfalling=fallingtimes;
                }
                else{
                    if(fallingtimes==matrixrow){
                        stop=1;
                        stopfalling=fallingtimes;
                    }
                    matrix[fallingtimes+3][col]=matrix[fallingtimes+2][col];
                    matrix[fallingtimes+2][col]=matrix[fallingtimes+1][col];
                    matrix[fallingtimes+1][col]=matrix[fallingtimes][col];
                    matrix[fallingtimes][col]=0;
                }
            }
        }
        //------
        if(stop){
            for(int elimination=1;elimination<=fallingblock.row;elimination++){
                for(int col=0;col<matrixcol;col++){
                    //different for every function------
                    if(matrix[stopfalling+elimination][col]==0){
                        check=0;
                        end=1;
                        //cout << "yes again" << endl;
                        break;
                    }
                    else
                        check=1;
                }
                if(check){
                    for(int col=0;col<matrixcol;col++){
                        //different for every function------
                        matrix[stopfalling+elimination][col]=0;
                    }
                    //check=0;
                    eliminationlocation=elimination;
                    eliminationtimes++;
                }
            }
        }
        if(eliminationtimes>0){
            switch(eliminationtimes){
                case(0):
                    end=1;
                    break;
                case(1):
                    //different for every function
                    for(int row=stopfalling+eliminationlocation;row>0;row--){
                        for(int col=0;col<matrixcol;col++){
                            matrix[row][col]=matrix[row-1][col];
                        }
                    }
                    for(int col=0;col<matrixcol;col++){
                        matrix[0][col]=0;
                    }
                    end=1;
                    break;
                case(2):
                    //different for every function
                    for(int row=stopfalling+eliminationlocation;row>1;row--){
                        for(int col=0;col<matrixcol;col++){
                            matrix[row][col]=matrix[row-2][col];
                        }
                    }
                    for(int col=0;col<matrixcol;col++){
                        matrix[0][col]=0;
                        matrix[1][col]=0;
                    }
                    end=1;
                    break;
                case(3):
                    //different for every function
                    for(int row=stopfalling+eliminationlocation;row>2;row--){
                        for(int col=0;col<matrixcol;col++){
                            matrix[row][col]=matrix[row-3][col];
                        }
                    }
                    for(int col=0;col<matrixcol;col++){
                        matrix[0][col]=0;
                        matrix[1][col]=0;
                        matrix[2][col]=0;
                    }
                    end=1;
                    break;
                default:
                    cout << "Eliminationtimes error!" << endl;
                    end=1;
                    break;
            }
        }
        //stop=0;
        //end=1;
        /*cout << "Falling:" << fallingtimes << endl;
        for(int i=0;i<matrixrow+5;i++){
            for(int j=0;j<matrixcol;j++){
                cout << matrix[i][j];
            }
            cout << endl;
        }*/
        if(end)
            break;
        //cout << "Falling:" << fallingtimes << endl;
    }
}

template<class T>
void TetrisBattle41(T &fallingblock, int **matrix, int index, int matrixrow, int matrixcol, bool &endgame){
    bool check=0;
    bool stop=0;
    bool end=0;
    int eliminationtimes=0;
    int eliminationlocation=0;
    int stopfalling=0;
    //T1 fallingblock;
    for(int fallingtimes=0;fallingtimes<=matrixrow;fallingtimes++){
        //if(matrix[fallingtimes+3][col])
        for(int j=index-1;j<index+fallingblock.col-1;j++){
            if(matrix[fallingtimes+2][j]==1){
                if(matrix[fallingtimes+3][j]==1){
                    if(fallingtimes==1){
                        endgame=1;
                        //stop=1;
                        //end=1;
                        break;
                    }
                    else{
                        stop=1;
                        stopfalling=fallingtimes-1;
                        //fallingtimes=fallingtimes-1;
                    //cout << "yes" << endl;
                        break;
                    }
                }
            }
        }
        if(endgame)
            break;
        //different for every function------
        if(!stop){
            for(int col=index-1;col<index-1+fallingblock.col;col++){
                if(fallingtimes==0){
                    matrix[fallingtimes+3][col]=fallingblock.shape[3][col-index+1];
                    matrix[fallingtimes+2][col]=fallingblock.shape[2][col-index+1];
                    matrix[fallingtimes+1][col]=fallingblock.shape[1][col-index+1];
                    matrix[fallingtimes][col]=fallingblock.shape[0][col-index+1];
                }
                /*else if(matrix[fallingtimes+2][col]==0 && matrix[fallingtimes+3][col]==1){
                    matrix[fallingtimes+2][col]=matrix[fallingtimes+1][col];
                    matrix[fallingtimes+1][col]=matrix[fallingtimes][col];
                    matrix[fallingtimes][col]=0;
                    stop=1;
                    //cout << "yes right" << endl;
                }*/
                else{
                    if(fallingtimes==matrixrow){
                        stop=1;
                        stopfalling=fallingtimes;
                    }
                    matrix[fallingtimes+3][col]=matrix[fallingtimes+2][col];
                    matrix[fallingtimes+2][col]=matrix[fallingtimes+1][col];
                    matrix[fallingtimes+1][col]=matrix[fallingtimes][col];
                    matrix[fallingtimes][col]=matrix[fallingtimes-1][col];
                    matrix[fallingtimes-1][col]=0;
                }
            }
        }
        //------
        if(stop){
            for(int elimination=1;elimination<=fallingblock.row;elimination++){
                for(int col=0;col<matrixcol;col++){
                    //different for every function------
                    if(matrix[stopfalling+elimination-1][col]==0){
                        check=0;
                        //end=1;
                        //cout << "yes again" << endl;
                        break;
                    }
                    else
                        check=1;
                }
                if(check){
                    for(int col=0;col<matrixcol;col++){
                        //different for every function------
                        matrix[stopfalling+elimination-1][col]=0;
                    }
                    //check=0;
                    eliminationlocation=elimination;
                    eliminationtimes++;
                }
            }
        }
        //cout << "location=" << eliminationlocation << endl;
        //cout << "times=" << eliminationtimes << endl;
        if(eliminationtimes>0){
            switch(eliminationtimes){
                case(0):
                    end=1;
                    break;
                case(1):
                    //different for every function
                    for(int row=stopfalling+eliminationlocation-1;row>0;row--){
                        for(int col=0;col<matrixcol;col++){
                            matrix[row][col]=matrix[row-1][col];
                        }
                    }
                    for(int col=0;col<matrixcol;col++){
                        matrix[0][col]=0;
                    }
                    end=1;
                    break;
                case(2):
                    //different for every function
                    for(int row=stopfalling+eliminationlocation-1;row>1;row--){
                        for(int col=0;col<matrixcol;col++){
                            matrix[row][col]=matrix[row-2][col];
                        }
                    }
                    for(int col=0;col<matrixcol;col++){
                        matrix[0][col]=0;
                        matrix[1][col]=0;
                    }
                    end=1;
                    break;
                case(3):
                    //different for every function
                    for(int row=stopfalling+eliminationlocation-1;row>2;row--){
                        for(int col=0;col<matrixcol;col++){
                            matrix[row][col]=matrix[row-3][col];
                        }
                    }
                    for(int col=0;col<matrixcol;col++){
                        matrix[0][col]=0;
                        matrix[1][col]=0;
                        matrix[2][col]=0;
                    }
                    end=1;
                    break;
                case(4):
                    //different for every function
                    for(int row=stopfalling+eliminationlocation-1;row>3;row--){
                        for(int col=0;col<matrixcol;col++){
                            matrix[row][col]=matrix[row-4][col];
                        }
                    }
                    for(int col=0;col<matrixcol;col++){
                        matrix[0][col]=0;
                        matrix[1][col]=0;
                        matrix[2][col]=0;
                        matrix[3][col]=0;
                    }
                    end=1;
                    break;
                default:
                    cout << "Eliminationtimes error!" << endl;
                    end=1;
                    break;
            }
        }
        //stop=0;
        //end=1;

        if(end)
            break;
        //cout << "Falling:" << fallingtimes << endl;
    }
}

template<class T>
void TetrisBattle14(T &fallingblock, int **matrix, int index, int matrixrow, int matrixcol, bool &endgame){
    bool check=0;
    bool stop=0;
    bool end=0;
    int eliminationtimes=0;
    int eliminationlocation=0;
    int stopfalling=0;
    //T1 fallingblock;
    for(int fallingtimes=0;fallingtimes<=matrixrow;fallingtimes++){
        //if(matrix[fallingtimes+3][col])
        for(int j=index-1;j<index+fallingblock.col-1;j++){
            if(matrix[fallingtimes+2][j]==1){
                if(matrix[fallingtimes+3][j]==1){
                    if(fallingtimes==1){
                        endgame=1;
                        //stop=1;
                        //end=1;
                        break;
                    }
                    else{
                        stop=1;
                        stopfalling=fallingtimes-1;
                        //fallingtimes=fallingtimes-1;
                    //cout << "yes" << endl;
                        break;
                    }
                }
            }
        }
        if(endgame)
            break;
        //different for every function------
        if(!stop){
            for(int col=index-1;col<index-1+fallingblock.col;col++){
                if(fallingtimes==0){
                    matrix[fallingtimes+3][col]=fallingblock.shape[0][col-index+1];
                }
                else{
                    if(fallingtimes==matrixrow){
                        stop=1;
                        stopfalling=fallingtimes;
                    }
                    matrix[fallingtimes+3][col]=matrix[fallingtimes+2][col];
                    matrix[fallingtimes+2][col]=0;
                }
            }
        }
        //------
        if(stop){
            for(int elimination=1;elimination<=fallingblock.row;elimination++){
                for(int col=0;col<matrixcol;col++){
                    //different for every function------
                    if(matrix[stopfalling+elimination+2][col]==0){
                        check=0;
                        //end=1;
                        //cout << "yes again" << endl;
                        break;
                    }
                    else
                        check=1;
                }
                if(check){
                    for(int col=0;col<matrixcol;col++){
                        //different for every function------
                        matrix[stopfalling+elimination+2][col]=0;
                    }
                    //check=0;
                    eliminationlocation=elimination;
                    eliminationtimes++;
                }
            }
        }
        if(eliminationtimes>0){
            switch(eliminationtimes){
                case(0):
                    end=1;
                    break;
                case(1):
                    //different for every function
                    for(int row=stopfalling+eliminationlocation+2;row>0;row--){
                        for(int col=0;col<matrixcol;col++){
                            matrix[row][col]=matrix[row-1][col];
                        }
                    }
                    for(int col=0;col<matrixcol;col++){
                        matrix[0][col]=0;
                    }
                    end=1;
                    break;
                default:
                    cout << "Eliminationtimes error!" << endl;
                    end=1;
                    break;
            }
        }
        //stop=0;
        //end=1;

        if(end)
            break;
        //cout << "Falling:" << fallingtimes << endl;
    }
}

template<class T>
void TetrisBattleO(T &fallingblock, int **matrix, int index, int matrixrow, int matrixcol, bool &endgame){
    bool check=0;
    bool stop=0;
    bool end=0;
    int eliminationtimes=0;
    int eliminationlocation=0;
    int stopfalling=0;
    //T1 fallingblock;
    for(int fallingtimes=0;fallingtimes<=matrixrow;fallingtimes++){
        //if(matrix[fallingtimes+3][col])
        for(int j=index-1;j<index+fallingblock.col-1;j++){
            if(matrix[fallingtimes+2][j]==1){
                if(matrix[fallingtimes+3][j]==1){
                    if(fallingtimes==1){
                        endgame=1;
                        //stop=1;
                        //end=1;
                        break;
                    }
                    else{
                        stop=1;
                        stopfalling=fallingtimes-1;
                        //fallingtimes=fallingtimes-1;
                    //cout << "yes" << endl;
                        break;
                    }
                }
            }
        }
        if(endgame)
            break;
        if(!stop){
            for(int col=index-1;col<index-1+fallingblock.col;col++){
                if(fallingtimes==0){
                    matrix[fallingtimes+3][col]=fallingblock.shape[1][col-index+1];
                    matrix[fallingtimes+2][col]=fallingblock.shape[0][col-index+1];
                }
                else{
                    if(fallingtimes==matrixrow){
                        stop=1;
                        stopfalling=fallingtimes;
                    }
                    matrix[fallingtimes+3][col]=matrix[fallingtimes+2][col];
                    matrix[fallingtimes+2][col]=matrix[fallingtimes+1][col];
                    matrix[fallingtimes+1][col]=0;
                }
            }
        }
        if(stop){
            for(int elimination=1;elimination<=fallingblock.row;elimination++){
                for(int col=0;col<matrixcol;col++){
                    if(matrix[stopfalling+elimination+1][col]==0){
                        check=0;
                        //end=1;
                        //cout << "yes again" << endl;
                        break;
                    }
                    else
                        check=1;
                }
                if(check){
                    for(int col=0;col<matrixcol;col++){
                        matrix[stopfalling+elimination+1][col]=0;
                    }
                    //check=0;
                    eliminationlocation=elimination;
                    eliminationtimes++;
                }
            }
        }
        if(eliminationtimes>0){
            switch(eliminationtimes){
                case(0):
                    end=1;
                    break;
                case(1):
                    //different for every function
                    for(int row=stopfalling+eliminationlocation+1;row>0;row--){
                        for(int col=0;col<matrixcol;col++){
                            matrix[row][col]=matrix[row-1][col];
                        }
                    }
                    for(int col=0;col<matrixcol;col++){
                        matrix[0][col]=0;
                    }
                    end=1;
                    break;
                case(2):
                    //different for every function
                    for(int row=stopfalling+eliminationlocation+1;row>1;row--){
                        for(int col=0;col<matrixcol;col++){
                            matrix[row][col]=matrix[row-2][col];
                        }
                    }
                    for(int col=0;col<matrixcol;col++){
                        matrix[0][col]=0;
                        matrix[1][col]=0;
                    }
                    end=1;
                    break;
                default:
                    cout << "Eliminationtimes error!" << endl;
                    end=1;
                    break;
            }
        }
        if(end)
            break;
        //cout << "Falling:" << fallingtimes << endl;
    }
}
int main(){
    T1 fallingblockT1;
    T2 fallingblockT2;
    T3 fallingblockT3;
    T4 fallingblockT4;
    L1 fallingblockL1;
    L2 fallingblockL2;
    L3 fallingblockL3;
    L4 fallingblockL4;
    J1 fallingblockJ1;
    J2 fallingblockJ2;
    J3 fallingblockJ3;
    J4 fallingblockJ4;
    S1 fallingblockS1;
    S2 fallingblockS2;
    Z1 fallingblockZ1;
    Z2 fallingblockZ2;
    I1 fallingblockI1;
    I2 fallingblockI2;
    O  fallingblockO;
    ifstream file1;
    int m,n; //m=matrixrow,n=matrixcol
    int **matrix;
    int initial=1;
    bool endgame=0;
    file1.open("Tetris.data");
    string str;
    int index;
    //讀取matrix大小
    if(!file1){
        cout << "File1 open fail!" << endl;
    }
    if(initial){
        file1 >> m >> n;
        initial=0;
    }
    //放大matrix
    m=m+5;
    matrix=new int*[m];
    for(int i=0;i<m;i++){
        matrix[i]=new int[n];
    }
    //印出matrix並初始化為0
    for(int i=0;i<m-1;i++){
        for(int j=0;j<n;j++){
            matrix[i][j]=0;
            //cout << matrix[i][j];
        }
        //cout << endl;
    }
    for(int j=0;j<n;j++){
        matrix[m-1][j]=1;
        //cout << matrix[m-1][j];
    }
    //cout << endl;
    //cout << fallingblockI1.col;
    while(file1 >> str && endgame!=1){
        if(str!="End"){
            file1 >> index;
            //cout << str << " " << index << endl;
            switch(str[0]){
                case 'T':
                    switch(str[1]){
                        case '1':
                            TetrisBattle23(fallingblockT1,matrix,index,m-5,n,endgame);
                            //cout << "endgame=" << endgame << endl;
                            /*for(int fallingtimes=0;fallingtimes<=m-4;fallingtimes++){
                                for(int col=index-1;col<index-1+fallingblockT1.col;col++){
                                    matrix[fallingtimes+3][col]=fallingblockT1.shape[1][col-index+1];
                                    matrix[fallingtimes+2][col]=fallingblockT1.shape[0][col-index+1];
                                    matrix[fallingtimes+1][col]=0;
                                }
                                cout << "Falling:" << fallingtimes << endl;
                            }*/
                            break;
                        case '2':
                            TetrisBattle32(fallingblockT2,matrix,index,m-5,n,endgame);
                            break;

                        case '3':
                            TetrisBattle23(fallingblockT3,matrix,index,m-5,n,endgame);
                            break;

                        case '4':
                            TetrisBattle32(fallingblockT4,matrix,index,m-5,n,endgame);
                            break;
                    }
                    break;
                case 'L':
                    switch(str[1]){
                        case '1':
                            TetrisBattle32(fallingblockL1,matrix,index,m-5,n,endgame);
                            break;
                        case '2':
                            TetrisBattle23(fallingblockL2,matrix,index,m-5,n,endgame);
                            break;
                        case '3':
                            TetrisBattle32(fallingblockL3,matrix,index,m-5,n,endgame);
                            break;
                        case '4':
                            TetrisBattle23(fallingblockL4,matrix,index,m-5,n,endgame);
                            break;

                    }
                    break;
                case 'J':
                    switch(str[1]){
                        case '1':
                            TetrisBattle32(fallingblockJ1,matrix,index,m-5,n,endgame);
                            break;
                        case '2':
                            TetrisBattle23(fallingblockJ2,matrix,index,m-5,n,endgame);
                            break;
                        case '3':
                            TetrisBattle32(fallingblockJ3,matrix,index,m-5,n,endgame);
                            break;
                        case '4':
                            TetrisBattle23(fallingblockJ4,matrix,index,m-5,n,endgame);
                            break;
                    }
                    break;
                case 'S':
                    switch(str[1]){
                        case '1':
                            TetrisBattle23(fallingblockS1,matrix,index,m-5,n,endgame);
                            break;
                        case '2':
                            TetrisBattle32(fallingblockS2,matrix,index,m-5,n,endgame);
                            break;
                    }
                    break;
                case 'Z':
                    switch(str[1]){
                        case '1':
                            TetrisBattle23(fallingblockZ1,matrix,index,m-5,n,endgame);
                            break;
                        case '2':
                            TetrisBattle32(fallingblockZ2,matrix,index,m-5,n,endgame);
                            break;
                    }
                    break;
                case 'I':
                    switch(str[1]){
                        case '1':
                            TetrisBattle41(fallingblockI1,matrix,index,m-5,n,endgame);
                            break;
                        case '2':
                            TetrisBattle14(fallingblockI2,matrix,index,m-5,n,endgame);
                            break;
                    }
                    break;
                case 'O':
                    TetrisBattleO(fallingblockO,matrix,index,m-5,n,endgame);
                    break;
                //default:
            }
        }
        else{
            cout << "End!" << endl;
        }
    }
    for(int i=4;i<m-1;i++){
        for(int j=0;j<n;j++){
            cout << matrix[i][j];
        }
        cout << endl;
    }
    //cout << matrix[0][0];
    //file1.close();
    ofstream file2("Tetris.output");
    //file2.open("Tetris.output");
    if(!file2){
        cout << "File2 open fail!" << endl;
    }
    else{
        for(int i=4;i<m-1;i++){
            for(int j=0;j<n;j++){
                file2 << matrix[i][j];
            }
            file2 << endl;
        }
    }
    file1.close();
    file2.close();
    //記憶體釋放
    for(int i=0;i<m;i++)
        delete[] matrix[i];
    delete[] matrix;
}
