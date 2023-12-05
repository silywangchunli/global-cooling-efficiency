## ----------------------------------
# Title: Fraction-dependent variations in cooling efficiency of urban trees across global cities
# Objective: To quantify the seasonal CE in cities of North hemisphere and South hemisphere
# Created by: Chunli Wang
# Created on: 2023-12-5
# Copyright (c) Chunli Wang, 2023
# Nanjing University
# Email: chunliwayi@foxmail.com
## ----------------------------------


# -*- coding: utf-8 -*-
"""
Created on Mon Jul 18 21:27:59 2022

@author: ll
"""
# -*- coding: utf-8 -*-
"""
Created on Mon May  9 16:51:37 2022

@author: ll
"""
import os
import csv
import pandas as pd
import numpy as np
import glob

#对文件夹下所有文件每行求平均值
def cal_avg(filePath:str,outFilePath:str):
    all_files = glob.glob(filePath)
    print (all_files)
    # all_data_frames =[]
    
    for file in all_files:
        data_frame = pd.read_csv(file)
        data_frame = pd.DataFrame(data_frame).drop(['system:index','null_flag','.geo'],axis =1)
        data_frame['mean'] = pd.DataFrame(data_frame).iloc[:,3:].mean(axis=1)
        data_frame['std']  = pd.DataFrame(data_frame).iloc[:,3:].std(axis=1)

        data_frame['mean_Ec'] = pd.DataFrame(data_frame)[['0_Ec','1_Ec','month_2_day','month_3_day',
                                                  'month_4_day','month_5_day','month_6_day','month_7_day',
                                                  'month_8_day','month_9_day','month_10_day','month_11_day']].mean(axis=1)
        data_frame['std_Ec'] = pd.DataFrame(data_frame)[['month_0_day','month_1_day','month_2_day','month_3_day',
                                                  'month_4_day','month_5_day','month_6_day','month_7_day',
                                                  'month_8_day','month_9_day','month_10_day','month_11_day']].std(axis=1)
        data_frame['mean_night'] = pd.DataFrame(data_frame)[['month_0_night','month_1_night','month_2_night','month_3_night',
                                                  'month_4_night','month_5_night','month_6_night','month_7_night',
                                                  'month_8_night','month_9_night','month_10_night','month_11_night']].mean(axis=1)
        data_frame['std_night'] = pd.DataFrame(data_frame)[['month_0_night','month_1_night','month_2_night','month_3_night',
                                                  'month_4_night','month_5_night','month_6_night','month_7_night',
                                                  'month_8_night','month_9_night','month_10_night','month_11_night']].std(axis=1)
        
        #Nouth season
        
        data_frame['spr_day'] = pd.DataFrame(data_frame)[['month_2_day','month_3_day','month_4_day']].mean(axis=1)
        data_frame['spr_std_day'] = pd.DataFrame(data_frame)[['month_2_day','month_3_day','month_4_day']].std(axis=1)
        data_frame['spr_night'] = pd.DataFrame(data_frame)[['month_2_night','month_3_night','month_4_night']].mean(axis=1)
        data_frame['spr_std_night'] = pd.DataFrame(data_frame)[['month_2_night','month_3_night','month_4_night']].std(axis=1)
        
        data_frame['sum_day'] = pd.DataFrame(data_frame)[['month_5_day','month_6_day','month_7_day']].mean(axis=1)
        data_frame['sum_std_day'] = pd.DataFrame(data_frame)[['month_5_day','month_6_day','month_7_day']].std(axis=1)
        data_frame['sum_night'] = pd.DataFrame(data_frame)[['month_5_night','month_6_night','month_7_night']].mean(axis=1)
        data_frame['sum_std_night'] = pd.DataFrame(data_frame)[['month_5_night','month_6_night','month_7_night']].std(axis=1)
        
        data_frame['aut_day'] = pd.DataFrame(data_frame)[['month_8_day','month_9_day','month_10_day']].mean(axis=1)
        data_frame['aut_std_day'] = pd.DataFrame(data_frame)[['month_8_day','month_9_day','month_10_day']].std(axis=1)
        data_frame['aut_night'] = pd.DataFrame(data_frame)[['month_8_night','month_9_night','month_10_night']].mean(axis=1)
        data_frame['aut_std_night'] = pd.DataFrame(data_frame)[['month_8_night','month_9_night','month_10_night']].std(axis=1)
        
        data_frame['win_day'] = pd.DataFrame(data_frame)[['month_11_day','month_0_day','month_1_day']].mean(axis=1)
        data_frame['win_std_day'] = pd.DataFrame(data_frame)[['month_11_day','month_0_day','month_1_day']].std(axis=1)
        data_frame['win_night'] = pd.DataFrame(data_frame)[['month_11_night','month_0_night','month_1_night']].mean(axis=1)
        data_frame['win_std_night'] = pd.DataFrame(data_frame)[['month_11_night','month_0_night','month_1_night']].std(axis=1)
         
        # South season
        # data_frame['spr_day'] = pd.DataFrame(data_frame)[['month_8_day','month_9_day','month_10_day']].mean(axis=1)
        # data_frame['spr_std_day'] = pd.DataFrame(data_frame)[['month_8_day','month_9_day','month_10_day']].std(axis=1)
        # data_frame['spr_night'] = pd.DataFrame(data_frame)[['month_8_night','month_9_night','month_10_night']].mean(axis=1)
        # data_frame['spr_std_night'] = pd.DataFrame(data_frame)[['month_8_night','month_9_night','month_10_night']].std(axis=1)
        
        # data_frame['sum_day'] = pd.DataFrame(data_frame)[['month_11_day','month_0_day','month_1_day']].mean(axis=1)
        # data_frame['sum_std_day'] = pd.DataFrame(data_frame)[['month_11_day','month_0_day','month_1_day']].std(axis=1)
        # data_frame['sum_night'] = pd.DataFrame(data_frame)[['month_11_night','month_0_night','month_1_night']].mean(axis=1)
        # data_frame['sum_std_night'] = pd.DataFrame(data_frame)[['month_11_night','month_0_night','month_1_night']].std(axis=1)
        
        # data_frame['aut_day'] = pd.DataFrame(data_frame)[['month_2_day','month_3_day','month_4_day']].mean(axis=1)
        # data_frame['aut_std_day'] = pd.DataFrame(data_frame)[['month_2_day','month_3_day','month_4_day']].std(axis=1)
        # data_frame['aut_night'] = pd.DataFrame(data_frame)[['month_2_night','month_3_night','month_4_night']].mean(axis=1)
        # data_frame['aut_std_night'] = pd.DataFrame(data_frame)[['month_2_night','month_3_night','month_4_night']].std(axis=1)
        
        # data_frame['win_day'] = pd.DataFrame(data_frame)[['month_5_day','month_6_day','month_7_day']].mean(axis=1)
        # data_frame['win_std_day'] = pd.DataFrame(data_frame)[['month_5_day','month_6_day','month_7_day']].std(axis=1)
        # data_frame['win_night'] = pd.DataFrame(data_frame)[['month_5_night','month_6_night','month_7_night']].mean(axis=1)
        # data_frame['win_std_night'] = pd.DataFrame(data_frame)[['month_5_night','month_6_night','month_7_night']].std(axis=1)
        
        data_frame.to_csv(outFilePath,index=False)   

if __name__=='__main__':
    filePath = r'E:/global_final/drivers/all_factor/out_S/'
    outFilePath = r'E:/global_final/drivers/all_factor/out_S/'
    files = os.listdir(filePath)
    for file in files:
        currentFile = os.path.join(filePath,file)
        outputFile = os.path.join(outFilePath,file)
        cal_avg(currentFile,outputFile)
        print('{} finished!'.format(file))    



