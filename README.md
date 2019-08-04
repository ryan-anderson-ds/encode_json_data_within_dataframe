# encode_json_data_within_dataframe
Encode json data within a dataframe

Inputs:
* pandas_data_frame: A pandas dataframe with a json column within it
* json_column_index: index of that column
* json_id_column: the unique identifier of the data you're trying to extract, e.g. "id" or "name"
* encodinglimit: the maximum amount of codes you want to generate. to save processing time or ignore special cases. Default 1000.
* remove_non_encoded: you may not want to use data that was not encoded. Defaults to 1, which discards anything that did not have the top encodinglimit codes.

Example input:

![JSON movie data](https://rian-van-den-ander.github.io/images/algo/encoding_json/input.png "Algorithm input")


Example output:

![JSON movie data](https://rian-van-den-ander.github.io/images/algo/encoding_json/output.png "Algorithm output")

Example usage:

~~~~

dataset = pd.read_csv('tmdb_5000_movies.csv')
dataset = dataset[["revenue","genres"]]
dataset = dataset[0:2]

encode_json_column(dataset,1,"id")

~~~~