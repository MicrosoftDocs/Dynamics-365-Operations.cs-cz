---
title: Nesprávná hodnota pole v záznamu TaxTrans
description: Tento článek poskytuje informace o řešení potíží s nesprávnými hodnotami polí v záznamu TaxTrans.
author: EricWangChen
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6e7329ffdc04207116c92cb42e02750b176713fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899807"
---
# <a name="incorrect-field-value-in-taxtrans"></a>Nesprávná hodnota pole v záznamu TaxTrans

[!include [banner](../includes/banner.md)]

Pokud je hodnota pole v záznamu **TaxTrans** nesprávná, pokuste se problém vyřešit pomocí informací v tomto článku.

## <a name="overview-of-values"></a>Přehled hodnot
Následující seznam ukazuje, jak jsou záznamy **TaxTrans**, **TaxUncommitted** a **TmpTaxWorkTrans** podobné datové sady, ale fungují odlišně.

  - **TaxTrans** je konečný výsledek zaúčtované daňové transakce přetrvávající v databázi.
  - **TaxUncommitted** je přechodný vypočítaný daňový výsledek přetrvávající v databázi (pokud existuje), který bude použit později při účtování.
  - **TmpTaxWorkTrans** je dočasný vypočítaný výsledek daně v tabulce v paměti (typ tabulky = InMemory).

Pokud zjistíte hlavní příčinu nesprávnosti sloupce **TaxTrans**, zjistili jste také hlavní příčinu nesprávnosti sloupců **TaxUncommitted** nebo **TmpTaxWorkTrans**. Je to proto, že tyto tři sloupce jsou navzájem kopírovány.

Během výpočtu daně se obvykle generuje záznam **TmpTaxWorkTrans** a poté, pokud je to relevantní, se generuje záznam **TaxUncommitted**. Během účtování daní se generuje záznam **TaxTrans**.


## <a name="add-breakpoints"></a>Přidání zarážek
Pomocí následujících kroků přidáte zarážky: 

1. Přidejte rozšíření a zarážky do příkazů *insert()* a *update()* v rozšířeních, jak je znázorněno níže.

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. Alternativně můžete přidat zarážky přímo, když není zahrnut záznam **TaxUncommitted**.

     - *TaxTrans.insert()*, *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>Reprodukce a ladění

Po nastavení zarážek je každá změna perzistence dat viditelná během ladění. Chcete-li najít hlavní příčinu nesprávného sloupce **TaxTrans**, **TaxUncommitted** nebo **TmpTaxWorkTrans**, zkontrolujte a poznamenejte si následující položky:

- Poslední zarážka, kde je sloupec správný.
- První zarážka, kde je sloupec nesprávný.
- Co se děje mezi těmito dvěma body.

## <a name="determine-whether-customization-exists"></a>Zjištění, zda existuje přizpůsobení
Pokud jste dokončili kroky v předchozích částech, ale problém se vám nepodařilo vyřešit, zjistěte, zda existuje přizpůsobení. Pokud žádné přizpůsobení neexistuje, požádejte o pomoc podporu společnosti Microsoft.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

