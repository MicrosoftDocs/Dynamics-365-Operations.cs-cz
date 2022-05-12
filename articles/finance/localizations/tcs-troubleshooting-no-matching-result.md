---
title: Nebylo možné najít žádné odpovídající výsledky
description: Toto téma vysvětluje, jak odstranit chybu "Nebyl nalezen žádný odpovídající výsledek" ve službě Výpočet daně.
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
ms.openlocfilehash: c1a343b0b74645d40b0a2582749968cc0a56afd7
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645393"
---
# <a name="no-matching-result-could-be-found"></a>Nebylo možné najít žádné odpovídající výsledky

[!include [banner](../includes/banner.md)]

V tomto tématu jsou vysvětleny kroky k odstranění problémů, které můžete provést, pokud se ve službě Výpočet daně zobrazí chyba "Nebyl nalezen žádný odpovídající výsledek".

## <a name="symptom"></a>Příznak

Zobrazí se následující chybová zpráva: "Záhlaví/řádky - 1, skupina Tax, nebyl nalezen žádný odpovídající výsledek."

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
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
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

K problému dochází, pokud není funkce správně nastavena ve službě Regulatory Configuration Service (RCS).

## <a name="troubleshoot"></a>Řešení potíží

1. Stáhněte si soubor pro odstraňování problémů. Další informace viz [Povolení režimu ladění pro odstraňování potíží](tcs-troubleshooting-enable-debug-mode.md).
2. Porovnejte zadání výpočtu daňové služby s nastavením funkce a opravte problém s nastavením.

    Následující příklad ukazuje vstup výpočtu daňové služby.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    V následující tabulce je uvedena použitelnost daňových skupin v RCS.

    | Proces Header.Business | Jednotka Lines.Business | Hlavička.Ship From Zip Code | Daňová skupina |
    |-------------------------|---------------------|---------------------------|-----------|
    | Deník                 |                     |                           | Skupina A   |
    | Prodej                   |                     | 30160                     | Skupina B   |

    Podle vstupu pro výpočet daňové služby je hodnota **Obchodní proces** v záhlaví **Prodej** a hodnota **Odeslání z PSČ** v záhlaví je **30159**. Tento vstup je založen na nastavení pravidel použitelnosti v RCS. Protože neexistuje žádný odpovídající řádek, dojde k chybě.

    > [!NOTE]
    > Pokud je hodnota v pravidle použitelnosti prázdná, pravidlo platí pro jakoukoli hodnotu.

## <a name="mitigation"></a>Zmírnění dopadů

Tuto chybu zmírníte pomocí následujícího postupu:

1. V RCS přejděte na **Funkce globalizace** \> **Výpočet daně**.
2. Vytvořte novou verzi funkce.
3. Přidejte řádek pro odpovídající informace.

    | Proces Header.Business | Jednotka Lines.Business | Hlavička.Ship From Zip Code| Daňová skupina |
    |-------------------------|---------------------|--------------------------|-----------|
    | Deník                 |                     |                          | Skupina A   |
    | Prodej                   |                     | 30160                    | Skupina B   |
    | Prodej                   |                     | 30159                    | Skupina B   |

4. Zveřejněte verzi nastavení funkce.
5. V Microsoft Dynamics 365 Finance jděte na **Daň** \> **Nastavení** \> **Konfigurace daně** \> **Parametry výpočtu daně** a vyberte novou verzi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
