SQL-Housing-Dataset
-- Select the entire dataset to view it in its entirety
SELECT * 
FROM housing.dbo.housing

--Select only the street, neighborhood and housestyle columns from the dataset
SELECT neighborhood, housestyle, street
FROM housing.dbo.housing

--Drop Alley and PoolQC columns
ALTER TABLE housing.dbo.housing
DROP COLUMN alley, poolqc

--Select the roofstyle, exterior2nd and foundation on the condition that the housestle is a 2story building
SELECT roofstyle, exterior2nd, foundation
FROM housing.dbo.housing
WHERE housestyle = '2story'

--Find the mssubclass that is greater than 160
SELECT *
FROM housing.dbo.housing
WHERE MSSubClass > 160

--Find other roofstyles filtering out the Gable roofstyle
SELECT *
FROM housing.dbo.housing
WHERE RoofStyle > 'Gable'

--Select only the Gable roofstyle from the roofstyles
SELECT * 
FROM housing.dbo.Housing
WHERE Roofstyle = 'gable'

--Sum mssubclass, overallqual and overallcond and save in a column titled m_plus_0_minus_0
SELECT MSSubClass, OverallQual, OverallCond,
mssubclass + overallqual + overallcond AS M_plus_O_minus_O
FROM housing.dbo.housing 

