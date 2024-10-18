SELECT 
    MONTH(record_date) AS month, 
    MAX(CASE WHEN data_type = 'max' THEN data_value ELSE NULL END) AS monthly_maximum,
    MIN(CASE WHEN data_type = 'min' THEN data_value ELSE NULL END) AS monthly_minimum,
    ROUND(AVG(CASE WHEN data_type = 'avg' THEN data_value ELSE NULL END)) AS monthly_average
FROM 
    temperature_records
GROUP BY 
    MONTH(record_date);
