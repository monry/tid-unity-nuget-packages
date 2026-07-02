# NuGetPackages

東京情報デザイン専門職大学（TID: Tokyo Information Design Professional University）の講義で用いる Unity プロジェクトから参照される **NuGet パッケージ群を管理する**ためのリポジトリです。

## 概要

講義で使用する Unity プロジェクト本体とは分離し、[NuGetForUnity](https://github.com/GlitchEnzo/NuGetForUnity) で導入した NuGet パッケージを、この Unity ワークスペースで一括して復元・管理します。復元されたパッケージは `Assets/NuGetPackages/Packages/` 以下に配置され、講義用プロジェクトから参照されます。

| 項目 | 内容 |
| --- | --- |
| Unity エディターバージョン | `6000.3.19f1` |
| パッケージ管理 | [NuGetForUnity](https://github.com/GlitchEnzo/NuGetForUnity) v4.2.0 |
| パッケージ定義ファイル | [`Assets/packages.config`](Assets/packages.config) |
| パッケージ配置先 | [`Assets/NuGetPackages/Packages/`](Assets/NuGetPackages/Packages) |

## 導入している NuGet パッケージ

| パッケージ | バージョン | 著作者 | 説明 |
| --- | --- | --- | --- |
| [R3](https://github.com/Cysharp/R3) | 1.3.0 | Cysharp, Inc. | 新しい設計の Reactive Extensions（Rx）実装 |
| [Microsoft.Bcl.AsyncInterfaces](https://github.com/dotnet/runtime) | 6.0.0 | Microsoft | 非同期ストリーム向けインターフェイス群 |
| [Microsoft.Bcl.TimeProvider](https://github.com/dotnet/runtime) | 8.0.0 | Microsoft | 時刻抽象化 `TimeProvider` のバックポート |
| [System.ComponentModel.Annotations](https://github.com/dotnet/runtime) | 5.0.0 | Microsoft | データ検証用アノテーション属性 |
| [System.Runtime.CompilerServices.Unsafe](https://github.com/dotnet/runtime) | 6.0.0 | Microsoft | 低レベルなメモリ操作 API |
| [System.Threading.Channels](https://github.com/dotnet/runtime) | 8.0.0 | Microsoft | 生産者／消費者パターン向けチャネル |

> [!NOTE]
> `R3` のみが明示的に導入したパッケージ（`manuallyInstalled`）で、その他は `R3` が必要とする依存パッケージです。

## ライセンス表記 (Third-Party Licenses)

本リポジトリが同梱する NuGet パッケージは、いずれも **MIT License** の下で配布されています。各パッケージの著作権は、それぞれの原著作者に帰属します。以下より各パッケージのライセンス全文を参照できます。

| パッケージ | ライセンス | 著作権表示 | ライセンス全文 |
| --- | --- | --- | --- |
| R3 | MIT | © 2024 Cysharp, Inc. | [LICENSE](Assets/NuGetPackages/Packages/R3.1.3.0/LICENSE.md) |
| Microsoft.Bcl.AsyncInterfaces | MIT | © .NET Foundation and Contributors | [LICENSE.TXT](Assets/NuGetPackages/Packages/Microsoft.Bcl.AsyncInterfaces.6.0.0/LICENSE.TXT) |
| Microsoft.Bcl.TimeProvider | MIT | © .NET Foundation and Contributors | [LICENSE.TXT](Assets/NuGetPackages/Packages/Microsoft.Bcl.TimeProvider.8.0.0/LICENSE.TXT) |
| System.ComponentModel.Annotations | MIT | © .NET Foundation and Contributors | [LICENSE.TXT](Assets/NuGetPackages/Packages/System.ComponentModel.Annotations.5.0.0/LICENSE.TXT) |
| System.Runtime.CompilerServices.Unsafe | MIT | © .NET Foundation and Contributors | [LICENSE.TXT](Assets/NuGetPackages/Packages/System.Runtime.CompilerServices.Unsafe.6.0.0/LICENSE.TXT) |
| System.Threading.Channels | MIT | © .NET Foundation and Contributors | [LICENSE.TXT](Assets/NuGetPackages/Packages/System.Threading.Channels.8.0.0/LICENSE.TXT) |

> [!NOTE]
> `R3` は配布パッケージにライセンスファイルを同梱していないため、MIT License の条文同梱要件を満たすべく、[上流リポジトリ](https://github.com/Cysharp/R3/blob/main/LICENSE) の LICENSE を [`Assets/NuGetPackages/Packages/R3.1.3.0/LICENSE.md`](Assets/NuGetPackages/Packages/R3.1.3.0/LICENSE.md) として配置しています。
