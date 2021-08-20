---
title: Testy správy kvality
description: Toto téma popisuje, jak vytvořit testy, které bude možné použít pro objednávky kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62e5aca8c41aa324802e83e53f52ea39b623a65882962413e743e6dd2671a901
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781031"
---
# <a name="quality-management-tests"></a>Testy správy kvality

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vytvořit testy, které bude možné použít pro objednávky kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.

Stránku **Testy** použijete k definování a prohlížení individuálních testů, které zjišťují, zda vaše produkty splňují specifikace kvality. Ke skupině testů můžete přiřadit jeden nebo více individuálních testů. V tomto případě zadáte také informace specifické pro daný test, jako jsou například přijatelné hodnoty měření. Naměřené hodnoty se používají pro testy množství. Pro testy kvality se používají testovací proměnné.

- Pro testy množství je pole **Typ** nastaveno na hodnotu *Celé číslo* nebo *Zlomek*. Zadána je také měrná jednotka. Specifikace kvality a výsledky testu jsou vyjádřeny jako čísla.
- U testů kvality je pole **Typ** nastaveno na hodnotu *Možnost*. Testy kvality vyžadují další informace o měřených testovacích proměnných a o výčtu jejich hodnot. Specifikace kvality a výsledky testu jsou vyjádřeny v závislosti na výstupu.

Testovací přístroj lze volitelně přiřadit k testování. Testovací přístroje však nejsou nutné k vytváření a používání testů s objednávkami kvality. Další informace viz [Testovací přístroje pro řízení kvality](quality-test-instruments.md).

Můžete také volitelně určit jednotku pro test, abyste označili měrnou jednotku, ve které jsou zaznamenány výsledky testu. Například test teploty může zahrnovat jednotku buď stupňů Fahrenheita, nebo stupňů Celsia.

## <a name="example-of-a-test"></a>Příklad testu

Výrobní společnost provádí dva testy na zakoupeném materiálu: test množství ohledně kvality materiálu a test kvality ohledně poškození balení. Tato společnost určuje další informace ohledně testu kvality s cílem definovat testovací proměnnou (například poškozené balení) a její výsledky. Společnost používá stránku **Testovací skupiny** k přiřazení dvou testů do skupiny testů a k určení informací o daném testu. Testovací skupina je přiřazena k objednávce kvality, takže daná společnost může vytvořit sestavu výsledků testů pro dané dva testy.

## <a name="create-a-test"></a>Vytvoření testu

Při vytváření testu postupujte takto.

1. Přejděte k nabídce **Řízení zásob \> Nastavení \> Řízení kvality \> Testy**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Test** – zadejte jedinečné ID nebo název testu.
    - **Popis** – zadejte podrobný popis testu.
    - **Typ** – vyberte typ výsledků, které test produkuje. U testů množství vyberte *Zlomek* nebo *Celé číslo*. U testů kvality vyberte hodnotu *Možnost*.
    - **Testovací přístroj** – vyberte [testovací přístroj](quality-test-instruments.md), který má být použit pro test.
    - **Jednotka** – pokud jste vybrali *Zlomek* nebo *Celé číslo* v poli **Typ** (tj. je-li testem test množství), vyberte měrnou jednotku, ve které by měly být zaznamenány výsledky testu.

1. Zavřete stránku.

> [!NOTE]
> Po uložení testu již nebudete moci upravit pole **Typ** v mřížce. Pokud musíte změnit typ výsledků testu, které budou pro test zaznamenány, vyberte v podokně akcí možnost **Změnit testovací typ kvality**. V dialogovém okně **Změnit testovací typ kvality** nastavte pole **Nový typ** na požadovaný typ a poté výběrem tlačítka **OK** zavřete dialogové okno.

## <a name="additional-resources"></a>Další prostředky

- [Testovací nástroje pro řízení kvality](quality-test-instruments.md)
- [Testovací skupiny pro řízení kvality](quality-test-groups.md)
- [Testovací proměnné pro řízení kvality](quality-test-variables.md)
- [Přiřazení kvality](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
