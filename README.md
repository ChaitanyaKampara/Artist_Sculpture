# ARTIST SCULPTURE
ARTIST SCULPTURE :

1.) IMPORTING LIBRARIES :-
    
    * NUMPY 
    * PANDAS
    * SEABORN
    * MATPLOTLIB
    * HANDLING WARNINGS : 
       import warnings 
       warnings.filterwarnings("ignore")

2.) DEALING WITH NULL VALUES

    * ISNULL() 
      * Artist Reputation : 750
      * Height : 375
      * Width : 584 
      * Weight : 587
      * Material : 764
      * Transport : 1392
      * Remote Location : 771
    * DROPNA()

3.) RECTIFYING ERRORS IN DATA :
 
    * COST > 0
      * SHAPE CHANGE => (3362, 20) ---> (3030, 20)
    * DATE_FORMAT

4.) ENCODING CATEGORICAL VALUES :

    * LABELENCODER() ---> fit()
      * CATEGORICAL_LIST= ['Material', 'International', 'Express Shipment', 'Installation Included', 'Transport', 'Fragile','Customer Information', 'Remote Location']


5.) OUTLIER DETECTION :

    * USING BOXPLOTS
     * Height - 55 and above.
     * Width - 22 and above.
     * Price Of Sculpture - 100k and above
     * Cost - 1.5 * 10^6 and above

6.) CORRELATION MATRIX - HEATMAP :

     * sns.heatmap(X.corr())
     * correlation of price(cost) to that of artists reputation is very low.
     * price of the sculpture is very much correlated to the weight
       * WE CAN FIND SOME CORRELATED FEATURES FROM DATA BUT WE ARE NOT DELETING THEM .
       * REASON : THEY ARE CONTRIBUTING TO OUR OUTPUT COLUMN (TARGET VARIABLE)

7.) FEATURE ENGINEERING :

     * ADDING NEW FEATURE FROM EXISTING ONES :
       * Waiting time = Scheduled Date - Delivery Date

8.) MODEL SELECTION :

     * RANDOM FOREST : HIGH ACCURACY , SCALABILITY , INTERPRETABILITY , ROBUST TO OUTLIERS
       * HYPERPARAMETERS : # n_estimators = the number of decision trees to be included in the random forest (MORE N_ESTIMATERS MORE TRAINIMG TIME BUT BETTER PERFORMANCE
                           # n_jobs = number of CPU cores to use for training the random forest. When set to -1, it uses all available CPU cores, "which can speed up the training process" significantly
