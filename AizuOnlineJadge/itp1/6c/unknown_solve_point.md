****コード内容は"AizuOnlineJadge/itp1/6c/split_official_house.rb"参照***

# 不明点
多次元配列の要素変更時に、指定していない他の配列の要素まで変わってしまう
".map(&:object_id)"でhouse内の各オブジェクト番号を参照する。
各オブジェクト番号が同じ = 同一オブジェクトとして扱われる。
だから一つの配列(オブジェクト)を変えると、他の要素も同時に変わる

# 解決方法
mapメソッドで分割して、新たなオブジェクトとして配列に入れる
".map{Array.new()}" でそれぞれ別の配列を返す
それぞれのオブジェクトが別の物として扱われる

# 参照URL
[Rubyの配列で使えるメソッド、二次元配列の使い方](https://qiita.com/dddisk/items/8ad2d5570edf3c577eea)
