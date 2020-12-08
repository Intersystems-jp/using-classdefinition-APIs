# 外部ファイルのクラス定義情報を読んでクラスを生成するサンプル

## 概要

このサンプルでは、プロパティやメソッドなど設定項目を、外部のファイルを読み込みながら作成しています。

サンプルプログラムは、クラスメソッドとして処理を記述していますが、ルーチンで作成しても動作します。

## ファイル一覧

- README.md このファイル
- Utility.xml サンプルプログラムが含まれるクラス定義ファイル
- Customer-pro.txt Customerクラスの定義が含まれるファイル
- Company-pro.txt Companyクラスの定義が含まれるファイル
- Customer-method.txt Customerクラスのメソッド定義が含まれるファイル


## サンプルクラスメソッド詳細


### クラスメソッド＝CreatePro　（プロパティ追加用）

- 引数1：パッケージ名.クラス名　→　作成されたい名前
- 引数2：読込みファイル（フルパス指定）→設定したいプロパティ
- 引数3：ファイルのデリミタ（省略時タブが使用されます） 　

#### サンプルファイル

- Customerクラス用＝Customer-pro.txt
- Companyクラス用＝Company-pro.txt 

#### ターミナルからの実行例

```
 Set file="C:\temp\Company-pro.txt"
 Do ##Class(ClassDef.Utility).CreateMethod("パッケージ名.クラス名",file)
```

### クラスメソッド＝CreateMethod （メソッド追加用）

- 引数1：パッケージ名.クラス名　→　追加対象のクラスを指定
- 引数2：読込みファイル（フルパス指定）→設定したいプロパティ
- 引数3：ファイルのデリミタ（省略時タブが使用される）

#### サンプルファイル

- Csutomerクラスへの追加用＝Customer-method.txt 

#### ターミナルからの実行例

```
 Set file="C:\temp\Customer-method.txt"
 Do ##Class(ClassDef.Utility).CreateMethod("パッケージ名.クラス名",file)
```

## スタジオでのサンプルファイルインポート方法

- スタジオ： `[ツール] > [ローカルからインポート] > [添付のXMLファイルを指定しインポート]`