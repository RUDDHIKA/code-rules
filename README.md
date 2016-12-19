# code-rules
					/*DOCTYPE C
													MINI PROJECT
						TOPIC IS 					MINI ATLAS
					*/		
#include<stdio.h>
#include<string.h>
#define begin main
int rivers(void);
int waterfalls(void);
int oceansea(void);
int dam(void);
int peaks(void);
int deepseatrench(void);
int island(void);
int india(void);
int srilanka(void);
int unitedstates(void);
int africac(void);
int asiac(void);
int australiac(void);
int europec(void);
int northamericac(void);
int southamericac(void);
//stuctures used for the respective purposes
struct country
{
	char cname[50];
	char capital[50];
	char lang[50];
	char currency[30];
	long unsigned areas;
};

struct feature
{
	char name[100];
	double area;
};
struct water
{
	char name1[100];
	double height;
};
struct inland
{
	char name2[100];
	double sqarea;
};
struct ocean
{
	char name3[100];
	long unsigned lsqarea;
};
struct dam
{
	char name4[100];
	double height2;
};
struct peak
{
	char name5[100];
	double height3;
};
struct deep
{
	char name6[100];
	double depth;
};
struct island
{
	char name7[100];
	double sarea;
};
int waterfalls(void)
{
	FILE *hwater;
	int y;	
	struct water s1;
	//the input  code for entering the detais of the highest water falls 
	//the file is opened in binary write mode and the details are got through the structure
	/*
	hwater=fopen("highestwaterfalls.txt","wb+");
	printf("\nENTER THE NAMES OF THE WATER FALLS AND ITS HEIGHT IN METRES");
		for(y=0;y<16;y++)
			{
				printf("\nENTER THE NAME OF WATER FALLS %d :",y+1);			
				gets(s1.name1);
				printf("\nENTER THE HEIGHT OF WATER FALLS %d :",y+1);
				scanf("%ld",&s1.height);		
				fwrite(&s1,sizeof(s1),1,hwater);
			getchar();
		}
	fclose(hwater);
	*/
	//output code for the water falls
		hwater=fopen("highestwaterfalls.txt","rb+");
		printf("\n\t\t\tWATER FALLS\t\tHEIGHT IN METRES\n");
		printf("\t\t\t------------\t\t----------------\n");
		for(y=0;y<16;y++)
			{
				fread(&s1,sizeof(s1),1,hwater);
				if(strlen(s1.name1)>20)
				printf("\n\t\t\t%s\t\t%ld",s1.name1,s1.height);
				else if(strlen(s1.name1)>15)
				printf("\n\t\t\t%s\t\t%ld",s1.name1,s1.height);
				else
				printf("\n\t\t\t%s\t\t\t%ld",s1.name1,s1.height);
			}
		fclose(hwater);
	return 0;
}
int rivers(void)
{
	FILE *lriver;
	int y;
	struct feature s;
	//the input  code for entering the detais of the rivers
	//the file is opened in binary write mode and the details are got through the structure
	/*
	lriver=fopen("longestrivers.txt","wb+");
	printf("\nENTER THE NAMES OF THE RIVERS AND ITS LENGTH IN METRES");
		for(y=0;y<25;y++)
			{
				printf("\nENTER THE NAME OF RIVER  %d :",y+1);			
				gets(s.name);
				printf("\nENTER THE LENGTH OF THE RIVER %d :",y+1);
				scanf("%ld",&s.area);				
				fwrite(&s,sizeof(s),1,lriver);
				getchar();
			}
		fclose(lriver);
	*/
	//output code for the rivers
	lriver=fopen("longestrivers.txt","rb+");
		printf("\n\t\t\tRIVER\t\t\t\t\tLENGTH IN METRES\n");
		printf("\t\t\t--------\t\t\t\t----------------\n");
		for(y=0;y<25;y++)
			{
				fread(&s,sizeof(s),1,lriver);
				if(strlen(s.name)>24)
					printf("\n\t\t\t%s\t\t--%ld",s.name,s.area);
				else if(strlen(s.name)>15)
					printf("\n\t\t\t%s\t\t\t--%ld",s.name,s.area);
				else
					printf("\n\t\t\t%s\t\t\t\t--%ld",s.name,s.area);
			}
		fclose(lriver);
	return 0;
}
int deepseatrench(void)
{
	FILE *hdeep;
	int y;
	struct deep s6;
	//the input  code for entering the detais of the deep-sea trenches in the world
	//the file is opened in binary write mode and the details are got through the structure
	/*
	hdeep=fopen("deepsea.txt","wb+");
	printf("\nENTER THE NAMES OF THE DEAP SEA TRENCHES  AND ITS DEPTH IN METRES");
		for(y=0;y<11;y++)
			{
				printf("\nENTER THE NAME OF THE DEEP SEA %d :",y+1);			
				gets(s6.name6);
				printf("\nENTER THE DEPTH IN METRES %d :",y+1);
				scanf("%ld",&s6.depth);		
				fwrite(&s6,sizeof(s6),1,hdeep);
				getchar();
			}
	fclose(hdeep);
	*/
	//output code for deep-sea trenches in the world
		hdeep=fopen("deepsea.txt","rb+");
		printf("\n\t\t\tDEEP-SEA TRENCHES \t\t DEPTH IN METRES\n");
		printf("\t\t\t--------------------\t\t---------------\n");
		for(y=0;y<11;y++)
			{
				fread(&s6,sizeof(s6),1,hdeep);
				if(strlen(s6.name6)>23)
				printf("\n\t\t\t%s\t\t%ld",s6.name6,s6.depth);
				else
				printf("\n\t\t\t%s\t\t\t%ld",s6.name6,s6.depth);
			}
		fclose(hdeep);
	return 0;
}
int dam(void)
{
	FILE *mdam;
	int y;	
		struct dam s4;
	//the input  code for entering the detais of the major dams aaround the world
	//the file is opened in binary write mode and the details are got through the structure
		/*
	mdam=fopen("majordams.txt","wb+");
	printf("\nENTER THE NAMES OF THE DAMS AND ITS HEIGHT IN METRES");
		for(y=0;y<10;y++)
			{
				printf("\nENTER THE NAME OF THE DAM  %d :",y+1);			
				gets(s4.name4);
				printf("\nENTER THE HEIGHT IN METRES %d :",y+1);
				scanf("%ld",&s4.height2);		
				fwrite(&s4,sizeof(s4),1,mdam);
				getchar();
			}
	fclose(mdam);
	*/
	//output code for majaor dams 
		mdam=fopen("majordams.txt","rb+");
		printf("\t\t\tMAJOR DAMS \t\t HEIGHT IN METRES\n");
		printf("\t\t\t~~~~~~~~~~~~\t\t~~~~~~~~~~~~~~~~~~\n");
		printf("\t\t\tASIA");
		printf("\n\t\t\t------\n");
		for(y=0;y<3;y++)
			{
				fread(&s4,sizeof(s4),1,mdam);
				if(strlen(s4.name4)>23)
				printf("\n\t\t\t%s\t\t%ld",s4.name4,s4.height2);
				else
				printf("\n\t\t\t%s\t\t\t%ld",s4.name4,s4.height2);
			}
			printf("\n");
			printf("\n\t\t\tAFRICA");
			printf("\n\t\t\t--------\n");
		for(y=3;y<5;y++)
			{
				fread(&s4,sizeof(s4),1,mdam);
				if(strlen(s4.name4)>23)
				printf("\n\t\t\t%s\t\t%ld",s4.name4,s4.height2);
				else
				printf("\n\t\t\t%s\t\t\t%ld",s4.name4,s4.height2);
			}
				printf("\n");
			printf("\n\t\t\tEUROPE");
			printf("\n\t\t\t--------\n");
		for(y=5;y<7;y++)
			{
				fread(&s4,sizeof(s4),1,mdam);
				if(strlen(s4.name4)>23)
				printf("\n\t\t\t%s\t\t%ld",s4.name4,s4.height2);
				else
				printf("\n\t\t\t%s\t\t\t%ld",s4.name4,s4.height2);
			}
				printf("\n");
			printf("\n\t\t\tAMERICA");
			printf("\n\t\t\t---------");
			for(y=7;y<9;y++)
			{
				fread(&s4,sizeof(s4),1,mdam);
				if(strlen(s4.name4)>23)
				printf("\n\t\t\t%s\t\t%ld",s4.name4,s4.height2);
				else
				printf("\n\t\t\t%s\t\t\t%ld",s4.name4,s4.height2);
			}
				printf("\n");
			printf("\n\t\t\tAUSTRALIA\n");
			printf("\t\t\t----------");
			for(y=9;y<10;y++)
			{
				fread(&s4,sizeof(s4),1,mdam);
				if(strlen(s4.name4)>23)
				printf("\n\t\t\t%s\t\t%ld",s4.name4,s4.height2);
				else
				printf("\n\t\t\t%s\t\t\t%ld",s4.name4,s4.height2);
			}
		fclose(mdam);
	return 0;
}
int peaks(void)
{
	FILE *hpeak;
	int y;
	struct peak s5;
	//the input  code for entering the detais of the highest peaks in the world
	//the file is opened in binary write mode and the details are got through the structures 
	/*
	hpeak=fopen("highestpeaks.txt","wb+");
	printf("\nENTER THE NAMES THE PEAKS AND ITS HEIGHT METRES");
		for(y=0;y<28;y++)
			{
				printf("\nENTER THE NAME OF INLAND WATER %d :",y+1);			
				gets(s5.name5);
				printf("\nENTER THE AREA OF WATER IN SQ KM %d :",y+1);
				scanf("%ld",&s5.height3);		
				fwrite(&s5,sizeof(s5),1,hpeak);
				getchar();
			}
	fclose(hpeak);
	*/
	//output code for the highest peaks in the world
		hpeak=fopen("highestpeaks.txt","rb+");
		printf("\n\t\t\tHIGHEST PEAKS\t\t\tHEIGHT IN METRES\n");
		printf("\t\t\t~~~~~~~~~~~~~~~~\t\t~~~~~~~~~~~~~~~~\n");
		printf("\n\t\t\tASIA\t\t");
		printf("\n\t\t\t---------\n");
		for(y=0;y<11;y++)
			{
				fread(&s5,sizeof(s5),1,hpeak);
				if(strlen(s5.name5)>23)
				printf("\n\t\t\t%s\t\t%ld",s5.name5,s5.height3);
				else if (strlen(s5.name5)>15)
				printf("\n\t\t\t%s\t\t\t%ld",s5.name5,s5.height3);
				else
				printf("\n\t\t\t%s\t\t\t\t%ld",s5.name5,s5.height3);
			}
			printf("\n");
			printf("\n\t\t\tAFRICA\t\t");
			printf("\n\t\t\t---------\n");
		for(y=11;y<15;y++)
			{
				fread(&s5,sizeof(s5),1,hpeak);
				if(strlen(s5.name5)>23)
				printf("\n\t\t\t%s\t\t%ld",s5.name5,s5.height3);
				else if (strlen(s5.name5)>15)
				printf("\n\t\t\t%s\t\t\t%ld",s5.name5,s5.height3);
				else
				printf("\n\t\t\t%s\t\t\t\t%ld",s5.name5,s5.height3);
			}
			printf("\n");
		printf("\n\t\t\tEUROPE\t\t");
		printf("\n\t\t\t---------\n");
		for(y=15;y<16;y++)
			{
				fread(&s5,sizeof(s5),1,hpeak);
				if(strlen(s5.name5)>23)
				printf("\n\t\t\t%s\t\t%ld",s5.name5,s5.height3);
				else if (strlen(s5.name5)>15)
				printf("\n\t\t\t%s\t\t\t%ld",s5.name5,s5.height3);
				else
				printf("\n\t\t\t%s\t\t\t\t%ld",s5.name5,s5.height3);
			}
			printf("\n");
		printf("\n\t\t\tNORTH AMERICA\t");
		printf("\n\t\t\t-------------\n");		
		for(y=16;y<20;y++)
			{
				fread(&s5,sizeof(s5),1,hpeak);
				if(strlen(s5.name5)>23)
				printf("\n\t\t\t%s\t\t%ld",s5.name5,s5.height3);
				else if (strlen(s5.name5)>15)
				printf("\n\t\t\t%s\t\t\t%ld",s5.name5,s5.height3);
				else
				printf("\n\t\t\t%s\t\t\t\t%ld",s5.name5,s5.height3);
			}
			printf("\n");
		printf("\n\t\t\tSOUTH AMERICA\t");
		printf("\n\t\t\t--------------\n");
		for(y=20;y<25;y++)
			{
				fread(&s5,sizeof(s5),1,hpeak);
				if(strlen(s5.name5)>23)
				printf("\n\t\t\t%s\t\t%ld",s5.name5,s5.height3);
				else if (strlen(s5.name5)>15)
				printf("\n\t\t\t%s\t\t\t%ld",s5.name5,s5.height3);
				else
				printf("\n\t\t\t%s\t\t\t\t%ld",s5.name5,s5.height3);
			}
			printf("\n");
		printf("\n\t\t\tAUSTRALIA & NEW ZEALAND\t\n");
		printf("\n\t\t\t-------------------------\n");
		for(y=25;y<28;y++)
			{
				fread(&s5,sizeof(s5),1,hpeak);
				if(strlen(s5.name5)>23)
				printf("\n\t\t\t%s\t\t%ld",s5.name5,s5.height3);
				else if (strlen(s5.name5)>15)
				printf("\n\t\t\t%s\t\t\t%ld",s5.name5,s5.height3);
				else
				printf("\n\t\t\t%s\t\t\t\t%ld",s5.name5,s5.height3);
			}
		fclose(hpeak);
	return 0;
}
int island(void)
{
	FILE *misland;
	int y;	
	struct island s7;
	//the input  code for entering the detais of the major islands in the world
	//the file is opened in binary write mode and the details are got through the structure
	/*
	misland=fopen("majorisland.txt","wb+");
	printf("\nENTER THE NAMES OF THE ISLAND AND ITS AREA IN SQUARE KILOMETRES");
		for(y=0;y<32;y++)
			{
				printf("\nENTER THE NAME OF ISLAND  %d :",y+1);			
				gets(s7.name7);
				printf("\nENTER THE AREA  IN SQ KM %d :",y+1);
				scanf("%ld",&s7.sarea);		
				fwrite(&s7,sizeof(s7),1,misland);
				getchar();
			}
	fclose(misland);
	*/
	//output code for the islands
		misland=fopen("majorisland.txt","rb+");
		printf("\n\t\t\tMAJOR ISLANDS \t\tAREA IN SQUARE KILOMETRES");
		printf("\n\t\t\t--------------\t\t---------------------------\n");
		for(y=0;y<27;y++)
			{
				fread(&s7,sizeof(s7),1,misland);
				if(strlen(s7.name7)>15)
					printf("\n\t\t\t%s\t\t\t%ld",s7.name7,s7.sarea);
				else if(strlen(s7.name7)>7)
					printf("\n\t\t\t%s\t\t\t\t%ld",s7.name7,s7.sarea);
				else
					printf("\n\t\t\t%s\t\t\t\t\t%ld",s7.name7,s7.sarea);
			}
		fclose(misland);
	return 0;
}
int oceansea(void)
{
	FILE *mocean;
	int y;
	struct ocean s3;
	//the input  code for entering the detais of the the major oceans and seas
	//the file is opened in binary write mode and the details are got through the structure
	/*
	mocean=fopen("oceanandseas.txt","wb+");
	printf("\nENT THE NAMES OF THE OCEAN AND ITS AREA IN  LAKH SQUARE KILOMETRES");
		for(y=0;y<18;y++)
		{		
				printf("\nENTER THE NAME OF OCEAN %d :",y+1);			
				gets(s3.name3);
				printf("\nENTER THE AREA OF OCEAN IN LAKH SQ KM %d :",y+1);
				scanf("%lu",&s3.lsqarea);		
				fwrite(&s3,sizeof(s3),1,mocean);
				getchar();
			}
	fclose(mocean);
	*/
	//output code for ocean and seas
		mocean=fopen("oceanandseas.txt","rb+");
		printf("\n\t\t\tMAJOR OCEAN AND SEAS \t\tAREA IN LAKH SQUARE KILOMETRES");
		printf("\n\t\t\t---------------------\t\t-------------------------------\n");
		for(y=0;y<18;y++)
			{
				fread(&s3,sizeof(s3),1,mocean);
				if(strlen(s3.name3)>15)
				printf("\n\t\t\t%s\t\t%ld",s3.name3,s3.lsqarea);
				else if(strlen(s3.name3)>8)
				printf("\n\t\t\t%s\t\t\t%ld",s3.name3,s3.lsqarea);
				else
				printf("\n\t\t\t%s\t\t\t\t%ld",s3.name3,s3.lsqarea);
			}
		fclose(mocean);
	return 0;
}
//function to display srilanka !!!!
int srilanka()
{
    int a=10,b=0,c=10;
    char *bits="UFy!OJy UCt+UCBCl(J)YAs UKq PQk VPk UQj URi SUh SVg TVf+TWe SYd R[c Q]a MAA Bab IAA Ac] Mf] Mga Hha Gib Eja Ema Bna AoZ GpY GqX GrW FtV FuU FvT EwO JuQ KtP LsP LrN OqU JoW JmZ Kh^ Kda Kaa N[h OUm PNp SLs THu";
    a=bits[b];
    while(a!=0)
	{
		a=bits[b];
        b++;
        while(a>64)
		 {
            a--;          
            if (++c=='Z')
			 {
                c/= 9;
                putchar(c);
            } 
			else 
			{
                putchar(33^(b&1));
            }
        }
    }
    return 0;
}
//function to display the united states !!!!
int unitedstates()
{
    int a=10,b=0,c=10;
    char *bits="z+MCF z+MEC z+MDE z(LDF z*KEG) *QbO AFF NBA AbE ABF AHE NBA AbC ADA ACA AHL HeD ACA ACB AHD O~C N~D M~E L~F L~F M~G J~H K|H L|J KzJ MxL MuK QsN PbK ADL S_N ADK T]P ADJ WZQ ADK ZUR ACL ZTS ABI aOU ABH fKa+hHl aDa mB]";
    a=bits[b];
    while(a!=0)
	{
		a=bits[b];
        b++;
        while(a>64)
		 {
            a--;          
            if (++c=='Z')
			 {
                c/= 9;
                putchar(c);
            } 
			else 
			{
                putchar(33^(b&1));
            }
        }
	}
    return 0;
}
int africac(void)
{
	FILE *africa;
	int i;
	struct country s;
	//the input  code for entering the detais of the countries in africa
	//the file is opened in binary append mode and the details are got through the structures s
	/*
	africa=fopen("dafrica.txt","ab+");
	printf("\nENTER THE DETAILS OF THE COUNTRIES OF AFRICA");
	for(i=0;i<10;i++)
		{
			printf("\nNAME %d--",i+1);
			gets(s.cname);
			printf("\nCAPITAL %d--",i+1);
			gets(s.capital);
			printf("\nLANGUAGE %d--",i+1);
			gets(s.lang);
			printf("\nCURRENCY %d--",i+1);
			gets(s.currency);
			printf("\nAREA IN SQUARE KILO METRES %d--",i+1);
			scanf("%lu",&s.areas);
			fwrite(&s,sizeof(s),1,africa);
			getchar();
		}
	fclose(africa);
	*/
	//output code for africa
		africa=fopen("dafrica.txt","rb+");
		printf("\n\t\t\t\t\tAFRICA\n");
		for(i=0;i<54;i++)
		{
			fread(&s,sizeof(s),1,africa);
			printf("\nNAME : %s \n",s.cname);
			printf("CAPITAL : %s",s.capital);
			printf("\tLANGUAGE :%s",s.lang);
			printf("\tCURRENCY :%s",s.currency);
			printf("\tAREA : %lu sq.kms",s.areas);	
			printf("\n\n=========================================================================================================================================\n");	
		}
	fclose(africa);
	return 0;
}
int asiac()
{
	FILE *asia;
	int i;
	struct country s1;
	//the input  code for entering the detais of the countries in asia
	//the file is opened in binary append mode and the details are got through the structure s1
	/*
	asia=fopen("dasia.txt","ab+");
	printf("\nENTER THE DETAILS OF THE COUNTRIES OF ASIA");
	for(i=0;i<39;i++)
	{
			printf("\nNAME %d--",i+1);
			gets(s1.cname);
			printf("\nCAPITAL %d--",i+1);
			gets(s1.capital);
			printf("\nLANGUAGE %d--",i+1);
			gets(s1.lang);
			printf("\nCURRENCY %d--",i+1);
			gets(s1.currency);
			printf("\nAREA IN SQUARE KILO METRES %d--",i+1);
			scanf("%lu",&s1.areas);
			fwrite(&s1,sizeof(s1),1,asia);
		getchar();
		}
	fclose(asia);
	*/
	//output code for asia
	asia=fopen("dasia.txt","rb+");
	printf("\n\t\t\t\t\tASIA\n");
		for(i=0;i<49;i++)
		{
			fread(&s1,sizeof(s1),1,asia);
			printf("\nNAME :%s\n",s1.cname);
			printf("CAPITAL :%s",s1.capital);
			printf("\tLANGUAGE :%s",s1.lang);
			printf("\tCURRENCY :%s",s1.currency);
			printf("\tAREA  :%lu sq.kms",s1.areas);
			printf("\n\n=======================================================================================================================================\n");
		}
	fclose(asia);
	return 0;
}
int australiac()
{
	FILE *austra;
	int i;
	struct country s2;
	//the input  code for entering the detais of the countries in australia
	//the file is opened in binary write mode and the details are got through the structures s2
	/*
	austra=fopen("daustralia.txt","wb+");
	printf("\nENTER THE DETAILS OF THE COUNTRIES OF AUSTRALIA");
	for(i=0;i<14;i++)
		{
			printf("\nNAME %d--",i+1);
			gets(s2.cname);
			printf("\nCAPITAL %d--",i+1);
			gets(s2.capital);
			printf("\nLANGUAGE %d--",i+1);
			gets(s2.lang);
			printf("\nCURRENCY %d--",i+1);
			gets(s2.currency);
			printf("\nAREA IN SQUARE KILO METRES %d--",i+1);
			scanf("%lu",&s2.areas);
			fwrite(&s2,sizeof(s2),1,austra);
			getchar();
		}
	fclose(austra);
	*/
	//output code for australia
	austra=fopen("daustralia.txt","rb+");
	printf("\n\t\t\t\t\tAUSTRALIA");
		for(i=0;i<14;i++)
		{
			fread(&s2,sizeof(s2),1,austra);
			printf("\nNAME :%s \n",s2.cname);
			printf("CAPITAL :%s",s2.capital);
			printf("\tLANGUAGE :%s",s2.lang);
			printf("\tCURRENCY :%s",s2.currency);
			printf("\tAREA  :%lu sq.kms",s2.areas);
			printf("\n\n=================================================================================================================================\n");
		}
	fclose(austra);
	return 0;
}
int northamericac()
{
	FILE *namerica;
	int i;
	struct country s3;
	//the input  code for entering the detais of the countries in north america
	//the file is opened in binary write mode and the details are got through the structures s3
	/*
	namerica=fopen("dnamerica.txt","wb+");
	printf("\nENTER THE DETAILS OF THE COUNTRIES OF NORTH AMERICA");
	for(i=0;i<23;i++)
	{
			printf("\nNAME %d--",i+1);
			gets(s3.cname);
			printf("\nCAPITAL %d--",i+1);
			gets(s3.capital);
			printf("\nLANGUAGE %d--",i+1);
			gets(s3.lang);
			printf("\nCURRENCY %d--",i+1);
			gets(s3.currency);
			printf("\nAREA IN SQUARE KILO METRES %d--",i+1);
			scanf("%lu",&s3.areas);
			fwrite(&s3,sizeof(s3),1,namerica);
			getchar();
		}
	fclose(namerica);
	*/
	//output code for the north america
	namerica=fopen("dnamerica.txt","rb+");
	printf("\n\t\t\t\t\tNORTH AMERICA\n");
	for(i=0;i<23;i++)
		{
			fread(&s3,sizeof(s3),1,namerica);
			printf("\nNAME : %s \n",s3.cname);
			printf("CAPITAL : %s",s3.capital);
			printf("\tLANGUAGE :%s",s3.lang);
			printf("\tCURRENCY :%s",s3.currency);
			printf("\tAREA : %lu sq.kms",s3.areas);	
			printf("\n\n================================================================================================================================\n");	
		}
	fclose(namerica);
	return 0;
}
int southamericac()
{
	FILE *samerica;
	int i;
	struct country s4;
	//the input  code for entering the detais of the countries in south america
	//the file is opened in binary write mode and the details are got through the structures s4
	/*
	samerica=fopen("dsamerica.txt","wb+");
	printf("\nENTER THE DETAILS OF THE COUNTRIES OF SOUTH AMERICA");
	for(i=0;i<12;i++)
		{
			printf("\nNAME %d--",i+1);
			gets(s4.cname);
			printf("\nCAPITAL %d--",i+1);
			gets(s4.capital);
			printf("\nLANGUAGE %d--",i+1);
			gets(s4.lang);
			printf("\nCURRENCY %d--",i+1);
			gets(s4.currency);
			printf("\nAREA IN SQUARE KILO METRES %d--",i+1);
			scanf("%lu",&s4.areas);
		fwrite(&s4,sizeof(s4),1,samerica);
			getchar();
		}
	fclose(samerica);
	*/
	//output code for south america
	samerica=fopen("dsamerica.txt","rb+");
	printf("\n\t\t\t\t\tSOUTH AMERICA\n");
	for(i=0;i<12;i++)
	{
			fread(&s4,sizeof(s4),1,samerica);
			printf("\nNAME : %s \n",s4.cname);
			printf("CAPITAL : %s",s4.capital);
			printf("\tLANGUAGE :%s",s4.lang);
			printf("\tCURRENCY :%s",s4.currency);
			printf("\tAREA : %lusq.kms",s4.areas);	
			printf("\n\n================================================================================================================================\n");	
		}
	fclose(samerica);
	return 0;
}
int europec()
{
	FILE *europe;
	int i;
	struct country s5;
	//the input code for displaying the countries that are present in europe
	//the file is opened in binary write mode and the details are got through the structure s5
	/*
	europe=fopen("deurope.txt","wb+");
	printf("\nENTER THE DETAILS OF THE COUNTRIES OF EUROPE");
	for(i=0;i<44;i++)
		{
			printf("\nNAME %d--",i+1);
			gets(s5.cname);
			printf("\nCAPITAL %d--",i+1);
			gets(s5.capital);
			printf("\nLANGUAGE %d--",i+1);
		gets(s5.lang);
			printf("\nCURRENCY %d--",i+1);
			gets(s5.currency);
			printf("\nAREA IN SQUARE KILO METRES %d--",i+1);
			scanf("%lu",&s5.areas);
			fwrite(&s5,sizeof(s5),1,europe);
			getchar();
		}
	fclose(europe);
	*/
	//output code for europe
	europe=fopen("deurope.txt","rb+");
	printf("\n\t\t\t\t\t\tEUROPE\n");
		for(i=0;i<44;i++)
		{
			fread(&s5,sizeof(s5),1,europe);
			printf("\nNAME : %s \n",s5.cname);
			printf("CAPITAL : %s",s5.capital);
			printf("\tLANGUAGE :%s",s5.lang);
			printf("\tCURRENCY :%s",s5.currency);
			printf("\tAREA : %lu sq.kms",s5.areas);	
			printf("\n\n===============================================================================================================================\n");	
		}
	fclose(europe);	
	return 0;
}
int begin(void)
{
	int ch,n,g,f,i,a,h;
	char c[30];
	printf("\n\t\t\t\t\t\t\t\t\t\tWELCOME\t\t\t\t\t\t\t");
	//THE PROGRAM BEGINS
	do
	{
	printf("\nWHAT YOU WOULD LIKE TO DO \n1-DISPLAY COUNTRIES\n2-KNOW GOGRAPHICAL FEATURES OF THE WORLD\n3-KNOW ABOUT COUNTRIES  \n SAY :");
	scanf("%d",&g);
	switch(g)
	{
		case 1:
			//HAVE A VISUAL TREAT
			//THIS DIAPLAYS THE 3 COUNTRIES
			do
			{
			printf("\nENTER THE COUNTRY WHICH YOU WOULD LIKE TO PRINT ");
			printf("\n1-SRILANKA\n2-UNITED STATES \n SAY :");
			scanf("%d",&n);
				switch(n)
				{
					case 1:
						srilanka();
						break;
					case 2:
						unitedstates();
						break;
				}
				printf("\nPRESS '0' TO EXIT");
			}while(n>0);
			break;
		case 2:	
			//THIS DISPLAY THE GEOGRAPHICAL COMPARISON OF THE WORLD
			printf("\n ---ENTER YOUR CHOICE TO DISPLAY THE GEOGRAPHICAL COMPARISON OF THE WORLD---");
	    	do
			{
			printf("\n1-LONGEST RIVERS\n2-HIGHEST WATER_FALLS \n3-MAJOR OCEAN AND SEAS\n4-MAJOR DAMS\n5-HIGHEST PEAKS\n6-DEEP_SEA TRENCHES \n7-MAJOR ISLANDS \n SAY :");
			scanf("%d",&ch);
			switch(ch)
			{
				case 1:
					rivers();
					break;
				case 2:
					waterfalls();
					break;
				case 3:
					oceansea();
					break;
				case 4:
					 dam();
					break;
				case 5:
					peaks();
					break;
				case 6:
					deepseatrench();
					break;
				case 7:
					island();
					break;	
			}
				printf("\nPRESS '0'TO EXIT");
			}while(ch>0);
			break;
		case 3:
			//THIS PRINTS THE COUNTRIES IN THE RESPECCTIVE CONTINENTS
				printf("\nENTER THE CONTINENT TO DISPLAY THE COUNTRIES");
				do
				{
				printf("\n1-AFRICA\n2-ASIA \n3-AUSTRALIA \n4-EUROPE \n5-NORTH AMERICA \n6-SOUTH AMERICA");
				scanf("%d",&a);
				if(a==1)
					africac();
				else if(a==2)
					asiac();
				else if(a==3)
					australiac();
				else if(a==4)
					europec();
				else if(a==5)
					northamericac();
				else 
					southamericac();
				printf("\nPRESS '0'TO EXIT");
				}while(a>0);
		}
	}while(g>0);
	if(g==0)
	printf("\n-------------THANK YOU--------------\n");	
	return 0;
}
