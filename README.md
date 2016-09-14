# TAX-LAB
def calculate_tax(dic):
    result = {}
    for name in dic.keys():
       if dic[name] <= 1000:
          result[name] = 0 * dic[name]
       elif dic[name] <= 10000:
          result[name] = (0 * 1000) + (0.1 * (dic[name] - 1000))
       elif dic[name] <= 20200:
          result[name] = (0 * 1000) + (0.1 * (9000)) + ( 0.15 * (dic[name] - 10000))
       elif dic[name] <= 30750:
          result[name] = (0 * 1000) + (0.1 * (9000)) + (0.15 * (10200)) + (0.2 * (dic[name] - 20200))
       elif dic[name] <= 50000:
          result[name] = (0 * 1000) + (0.1 * (9000)) + (0.15 * (10200)) + (0.2 * (10550)) + (0.25 * (dic[name] - 30750))
       else:
          result[name] = (0 * 1000) + (0.1 * (9000)) + (0.15 * (10200)) + (0.2 * (10550)) + (0.25 * (19250)) + ( 0.30 * (dic[name] - 50000))
    return result
