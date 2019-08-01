# encode_json_data_within_dataframe
Encode json data within a dataframe

Inputs:
* pandas_data_frame: A pandas dataframe with a json column within it
* json_column_index: index of that column
* json_id_column: the unique identifier of the data you're trying to extract, e.g. "id" or "name"

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