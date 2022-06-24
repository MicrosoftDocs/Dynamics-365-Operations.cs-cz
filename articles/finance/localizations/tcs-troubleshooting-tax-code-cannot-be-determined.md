---
title: Daňový kód nelze určit
description: Tento článek vysvětluje, jak odstranit chybu "Kód daně nelze určit" ve službě Výpočet daně.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 6a74724de38cf362900277ab9addc8e6894f7689
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877852"
---
# <a name="tax-code-cannot-be-determined"></a>Daňový kód nelze určit

[!include [banner](../includes/banner.md)]

V tomto článku jsou vysvětleny kroky k odstranění problémů, které můžete provést, pokud se ve službě Výpočet daně zobrazí chyba "Kód daně nelze určit".

## <a name="symptom"></a>Příznak

Zobrazí se následující chybová zpráva: "Záhlaví/řádky - 1, kód daně nelze určit." Případně najdete chybu v souboru pro řešení problémů, jak je uvedeno v následujícím příkladu. Další informace viz [Povolení režimu ladění pro odstraňování potíží](tcs-troubleshooting-enable-debug-mode.md).

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Příčina

K problému pravděpodobně dochází, protože se daňová skupina a daňová skupina položky neprotínají.

## <a name="troubleshoot"></a>Řešení potíží

Chcete-li opravit problém, postupujte následovně.

1. V souboru pro odstraňování problémů ověřte, že byla určena daňová skupina a daňová skupina položky. Pokud jsou hodnoty polí **Skupina daně** a **Skupina daňové položky** prázdné, skupina daně a skupina daně položky nebyly určeny. Pokud byly stanoveny, výsledky mohou být nesprávné.

    Následuje příklad souboru pro odstraňování problémů.

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
                            "Adjustment": null
                        }
                    ],
                    "Measures": {
                        ...
                    },
                    ...
                }
            ]
        },
        ...
    }
    ```

2. Ověřte, že je povolena možnost **Přepsat daň z prodeje** na kartě **Nastavení** podrobností řádku prodejní objednávky.

    - Pokud je tato funkce povolena, jsou daňové kódy určeny hodnotami **Daňová skupina** a **Daňová skupina položky**, které zadáte na řádku transakce. Ověřte, zda jsou tyto hodnoty zadány správně.
    - Pokud není povolena, zkontrolujte, zda byly nastaveny správné hodnoty pro pole **Použitelnost daňové skupiny** a **Použitelnost daňové skupiny položky**. Více informací viz [Nebyl nalezen žádný odpovídající výsledek](tcs-troubleshooting-no-matching-result.md).

3. Pokud byly daňová skupina a daňová skupina položky určeny správně, určete, zda pro ně existuje nějaký průnik.

    1. V RCS jděte na **Daňové funkce** \> **Daňové kódy a skupiny** \> **Daňová skupina**.

        | Řádek.Daňová skupina | Kódy daně |
        |----------------|-----------|
        | Skupina A        | A         |

    2. Jděte na **Daňové funkce** \> **Daňové kódy a skupiny** \> **Skupina daňové položky**.

        | Line.Item Tax Group | Kódy daně |
        |---------------------|-----------|
        | Skupina B             | mld.         |

    Pokud neexistuje průnik daňové skupiny a daňové skupiny položky, daňový kód nebude určen.

## <a name="mitigation"></a>Zmírnění dopadů

1. Projděte každý krok v části [Odstraňování problémů](#troubleshoot) tohoto článku a podle potřeby opravte nastavení. Pokud nebyla správně určena daňová skupina a daňová skupina položky, získáte informace v tématu [Nebyl nalezen žádný odpovídající výsledek](tcs-troubleshooting-no-matching-result.md).
2. Pokud neexistuje průnik daňové skupiny a daňové skupiny položky, vytvořte v RCS novou verzi funkce a opravte nastavení.

    - Jděte na **Daňové funkce** \> **Daňové kódy a skupiny** > **Skupina daňové položky**.

        | Line.Item Tax Group | Kódy daně |
        |---------------------|-----------|
        | Skupina B             | A;B       |

    Daňový řád bude určen jako **A**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
