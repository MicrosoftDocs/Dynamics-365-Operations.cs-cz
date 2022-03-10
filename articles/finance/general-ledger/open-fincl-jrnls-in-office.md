---
title: Otevření šablon finančního deníku v aplikaci Office
description: Toto téma popisuje problémy, které mohou nastat při vytváření vlastních finančních deníků pomocí šablony Microsoft Excel.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8c0c8d8e2e9b1978523bea378f4e231d9ebe3d1e8ccdc11ad8578eac16b067cf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753521"
---
# <a name="open-financial-journal-templates-in-office"></a>Otevření šablon finančního deníku v aplikaci Office

[!include [banner](../includes/banner.md)]

Toto téma popisuje problémy, které mohou nastat při vytváření vlastních finančních deníků pomocí šablony Microsoft Excel.

## <a name="symptom"></a>Příznak

Vytvořili jste vlastní šablonu aplikace Excel pro finanční deníky, ale ta se nezobrazuje v nabídce **Otevřít řádky v aplikaci Excel**. Případně se v nabídce objeví, ale po výběru se otevře jiná šablona.

## <a name="resolution"></a>Řešení

Výchozí funkce Otevřít v aplikaci Excel používá kořenový zdroj dat (tabulku) aktuální stránky k určení, které šablony Office nebo datové entity se zobrazí jako možnosti v nabídce **Otevřít v aplikaci Excel**. Toto chování není ideální, protože finanční deníky používají stejné tabulky (LedgerJournalTable a LedgerJournalTrans) jako kořenový zdroj dat mnoha jiných typů deníků.

V případě finančních deníků je funkce Otevřít řádky v aplikaci Excel určena k zobrazení šablon, které jsou určeny pro deník, s nímž právě pracujete (např. pro finanční deník nebo deník plateb). Například šablona, která je určena k použití s deníkem plateb dodavatele, bude navržena tak, aby vynucovala váš primární účet jako účet dodavatele.

Pokud chcete zvýšit úroveň šablony tak, aby byla k dispozici v nabídkách **Otevřít řádky v aplikaci Excel** a **Otevřít v aplikaci Excel**, jednoduchou možností pro vývojáře je implementace rozhraní **LedgerIJournalExcelTemplate** a rozšíření třídy **DocuTemplateRegistrationBase**. V systému je implementováno mnoho příkladů tohoto přístupu. Jedním příkladem, který lze použít jako referenci, je rozhraní **LedgerDailyJournalExcelTemplate**, které bylo vytvořeno pro finanční deník (nebo denní deník).

Když je pro vaši šablonu implementováno rozhraní **LedgerIJournalExcelTemplate**, nabídka **Otevřít řádky v aplikaci Excel** filtruje šablony podle typu vašeho deníku a zobrazí pouze šablony, které jsou pro daný deník k dispozici. Rozhraní také poskytuje metodu ověření, která zajišťuje, že šablonu nelze otevřít pro deník, pokud nesplňuje požadavky na typ účtu. Můžete například určit, že typ účtu musí být **Dodavatel** nebo **Hlavní kniha**.

Další informace o této funkci najdete v části [Přidejte šablony do nabídky Otevřít řádky v aplikaci Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).
