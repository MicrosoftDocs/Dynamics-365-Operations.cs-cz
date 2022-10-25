---
title: Audit synchronizace zákaznických operací v centrále
description: Tento článek vysvětluje, jak auditovat synchronizaci zákaznických operací v Microsoft Dynamics 365 Commerce headqurters, což vám pomůže vyřešit jakékoli problémy uživatelů webu.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691066"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>Audit synchronizace zákaznických operací v centrále

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tento článek vysvětluje, jak auditovat synchronizaci zákaznických operací v Microsoft Dynamics 365 Commerce headqurters, což vám pomůže vyřešit jakékoli problémy uživatelů webu.

S tím, jak si organizace začínají osvojovat možnost vytvářet a upravovat zákazníky asynchronně, správci webu potřebují způsob, jak zobrazit a odstraňovat problémy s operacemi na základě požadavků uživatelů webu nebo selhání procesů. V těchto scénářích by správci webu měli být schopni auditovat operace vytváření a úprav zákazníků a opravovat případné chyby pomocí samoobslužného modelu.

## <a name="customer-synchronization-status"></a>Stav synchronizace odběratele

Pokud se přihlásíte fo asynchronního režimu řízení zákazníků a souvisejících funkcí, správci Commerce headquarters musí vytvořit a naplánovat opakovanou dávkovou úlohu pro **P-úlohu** **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** a úlohu **1010**, aby byli všichni zákazníci Async převedeni na zákazníky Sync v Commerce headquarters. K synchronizaci operací správy zákazníků dochází při každém spuštění těchto úloh. Více informací viz [Asynchronní režim vytváření zákazníků](async-customer-mode.md).

Jako vlastník firmy můžete provádět následující operace:

- Zobrazit všechny operace vytváření/úprav uživatelů webu. Podrobnosti zahrnují stav a časové razítko.
- Filtrujte operace pomocí libovolného pole a hodnot v tabulce zákazníků, abyste zúžili protokol auditu.
- Prohlédněte si stručný popis změn spolu s podrobnostmi o stavu, abyste porozuměli operacím na vysoké úrovni.
- V případě selhání upravte a opravte problematická pole a poté uložte a synchronizujte konkrétní operace zákazníka.

### <a name="elements-on-the-customer-synchronization-status-page"></a>Prvky na stránce stavu synchronizace zákazníka

Chcete-li zobrazit seznam všech asynchronních operací, v Commerce headquarters přejděte na **Commerce a Retail \> Zákazníci \> Stav synchronizace zákazníka**. Následující obrázek ukazuje příklad stránky **Stav synchronizace zákazníka**.

![Stránka stavu synchronizace zákazníků v Commerce headquarters.](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

Ve výchozím nastavení seznam operací synchronizace zákazníků na levé straně stránky **Stav synchronizace zákazníka** bsahuje následující sloupce:

- Název kanálu
- Účet zákazníka
- Asynchronní účet odběratele
- Časové razítko operace
- Stav synchronizace odběratele

V pravé horní části stránky jsou zobrazeny detaily zákaznického účtu, jako např hodnoty **Zákaznický účet**, **Operace Retail Async**, **Stav synchronizace zákazníka** a **Poslední známá chyba**.

Sekce **Změnit popis** obsahuje popis typu operace správy zákazníků, která byla spuštěna (například vytvoření zákazníka, aktualizace účtu nebo selhání synchronizace s podrobnostmi).

Sekce **Atributy zákazníka** obsahuje mřížku, která zobrazuje všechny atributy zákazníka spolu se starými a novými hodnotami. Tuto sekci můžete upravit, pokud chcete změnit hodnoty atributů zákazníka, abyste opravili chyby, a poté znovu synchronizovat.
