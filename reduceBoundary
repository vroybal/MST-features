def reduceBoundary(df, b_index = 50):

  df = deepcopy(df)

  nameset = [col for col in df if 'centroid' in col]

  for name in sorted(nameset):
    print(name)
    df = df[df[name] > b_index]
    df = df[df[name] < df[name].max()-b_index]
  
  return deepcopy(df)

def getMSTfromDF(df):
  mst = mist.GetMST(x=np.asarray(df.centroid0), y=np.asarray(df.centroid1), z=np.asarray(df.centroid2))
  degree, edge_length, branch_length, branch_shape, l_index, b_index = mst.get_stats(include_index=True) 

  return degree, edge_length, branch_length, branch_shape, l_index, b_index 
