---
title: Řízení pracovníků skladu
description: Tento článek popisuje, jak mobilní aplikace Řízení skladu pomáhá řídit a sledovat práci, kterou provádí zaměstnanci ve skladech.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage, WHSResetUserPassword
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a3261571f7ba43a79ee42afd8cdfe9b69cb83c01de3e4b2b89d2b0aae668ea2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757511"
---
# <a name="manage-warehouse-workers"></a>Řízení pracovníků skladu

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak mobilní aplikace Řízení skladu pomáhá řídit a sledovat práci, kterou provádí zaměstnanci ve skladech.

Používáte-li funkci řízení skladu, všechny skladové operace pracovníků jsou označovány jako *práce*. Práce jako například výdej, přemístění a inventura zásob na skladě se zaznamenává pomocí mobilního zařízení. Předtím, než pracovník skladu může pracovat, musí být přidružen k pracovníkovi v modulu Lidské zdroje. Každý účet **Pracovník** může mít asociováno více skladů, se kterými jsou uživatelé přidruženi. Tito pracovní uživatelé mohou pracovat v různých skladech a mohou mít různé úrovně přístupu do různých nabídek mobilního zařízení. Můžete považovat pracovní uživatele skladu jako více přihlášení pro vybraného pracovníka. Každý pracovní uživatel má výchozí sklad a konkrétní workflow jsou zveřejněny pomocí položek nabídky, které jsou k dispozici pro pracovní uživatele. 

Pro vytvoření nového uživatele práce na stránce **Pracovník** na kartě **Obecné** v části **Sklady** klepněte na položku **Pracovník**. Je nutné zadat ID uživatele, jméno uživatele, výchozí sklad a název nabídky. Tato nabídka se načte, když se uživatel přihlásí do portálu skladu pro mobilní zařízení a umožní vám definovat položky nabídky, ke kterým má uživatel přístup. 

Jako součást nastavení pro každého pracovního uživatele můžete také definovat určité workflow procesu. Můžete například použít pole **Je supervizorem cyklické inventury** a určíte tak, zda uživatel může provádět úpravy v nesrovnalostech cyklické inventury během operace inventury, nebo zda tyto úpravy je nejdříve nutné zkontrolovat jinou osobou.

## <a name="defining-labor-standards"></a>Definování pracovních norem
Na stránce **Mzdové standardy** můžete definovat metody výpočtu, které systém používá pro výpočet odhadovaného času, který vyžaduje určitý typ práce. Tuto definici lze nastavit na obecné úrovni nebo na určité úrovni. Můžete například definovat dobu, která má být vyžadována při zpracování výdeje prodejní objednávky podle hmotnosti pro určitou definici jednotky při použití konkrétního procesu výdeje. Současně můžete zaznamenat čas založený na metodě výpočtu, pro uložení operace vydávaných zásob na skladě. 

Chcete-li povolit používání pracovních norem, které jste definovali, je nutné vybrat možnost **Povolit pracovní normy** pro každý sklad, kde budou pracovní normy použity.

## <a name="monitoring-and-controlling-warehouse-work"></a>Sledování a řízení práce ve skladu
Na stránce **Veškerá práce** můžete sledovat a spravovat všechny práce, které jsou plánovány, probíhají a jsou dokončeny. Na této stránce můžete aktualizovat různé procesy, například přiřazení pracovního uživatele skladu a priorita práce. Můžete také přejít dolů k podrobnostem, které se vztahují k záhlaví práce a řádkům práce pro získání pochopení očekávaných nebo dokončených pracovních procesů. 

Aktivujete-li možnost **Pracovní normy** zobrazí se vám vypočítaný odhadovaný čas pro práci. Poté při zpracování práce se také zobrazí skutečný čas pro každou pracovní operaci. Tímto způsobem můžete porovnat odhadovaný čas s výpočty skutečného času. 

Kromě toho můžete využít odhadovaného času v pravidlech pro automatické rozdělení práce při tvorbě práce. Tímto způsobem můžete načíst zůstatek práce na základě očekávaného času k dokončení úlohy. 

Analýza času který se používá ke zpracování pracovních položek může pomoci zlepšit efektivitu pracovníka skladu. Následující sestavy jsou k dispozici pro pomoc s touto analýzou:

-   **Práce podle uživatele** – Tato sestava zobrazuje produktivitu pracovníka, která vychází ze skutečného času proti očekávanému času.
-   **Práce podle typu transakce práce** – Pomocí této sestavy můžete analyzovat nedostatky v procesech určitého skladu. Například si všimněte, že vyskladnění pro převodní příkazy trvají delší dobu tento týden než v předchozích týdnech. Potom můžete použít tyto informace pro další analýzu.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]