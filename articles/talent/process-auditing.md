---
title: Sledování změn v náborových datech
description: Funkce auditování procesů umožňuje sledovat, kdy se změní uchazeči, otevřené pracovní pozice nebo žádosti o práci z důvodů vykazování nebo shody.
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 803c935493a4080b8c1d0ef92bbe7db601f3ca03
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517520"
---
# <a name="track-changes-in-recruiting-data"></a>Sledování změn v náborových datech

Nyní můžete sledovat změny kandidátů, otevřených pracovních pozic a žádostí o práci pomocí zpracování auditu. To je užitečné z důvodů vykazování nebo shody.

Sledovaná data lze zobrazit v aplikaci Power BI pomocí konektoru OData. Další informace naleznete v tématu [Připojení ke kanálům OData v Power BI Desktop](https://docs.microsoft.com/en-us/power-bi/desktop-connect-odata).

## <a name="track-changes"></a>Sledovat změny
Chcete-li v datech náboru nastavit sledování změn, postupujte takto:

1. V [PowerApps](https://web.powerapps.com) vyberte příslušné prostředí.

2. Vyberte **Nastavení** (ikona ozubeného kola), zvolte možnost **Rozšířená přizpůsobení** a poté vyberte **Zdroje** v části **Vývojářské zdroje**. 

3. Na stránce **Vývojářské zdroje** zkopírujte hodnotu v poli **Hodnota rozhraní API webu instance**. Hodnota může například vypadat takto: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/.

4. Poté se můžete dotazovat na data z jedné z následujících entit:
  - Historie otevřené pozice (msdyn_jobopeninghistories)
  - Historie žádosti o práci (msdyn_jobapplicationhistories) 
  - Historie kandidáta (msdyn_candidatehistories)

## <a name="data-reported"></a>Vykazovaná data

V rámci auditu procesu jsou k dispozici následující data.

| Vykazovaná data | Popis |
| --- | --- |
| Změnil/a (msdyn_ChangedbyId) | Odkaz na uživatele |
| Vytvořeno dne (createdon) |  Datum a čas v UTC, kdy změna nastala |
| Typ změny (msdyn_changetype) | Jaká změna nastala |
| Společné hodnoty pro kandidáty, otevřené pracovní pozice, <br></br>a žádosti o práci | Vytvořeno<br></br>Aktualizováno |
| Historie žádosti o práci | Přidaný artefakt <br></br>Odstraněný artefakt |
| Historie otevřené pracovní pozice | TODO: přidán příspěvek <br></br>TODO: odebrán příspěvek <br></br>TODO: aktualizován příspěvek <br></br>TODO: přidán účastník <br></br>TODO: odebrán účastník |
| Historie kandidáta | Přidaný artefakt <br></br>Odstraněný artefakt <br></br>Přidána pracovní zkušenost <br></br>Odstraněna pracovní zkušenost <br></br>Přidáno vzdělání <br></br>Odstraněno vzdělání <br></br>Přidána dovednost <br></br>Odstraněna dovednost <br></br>Přidána značka <br></br>Odstraněna značka <br></br>Přidána sociální síť <br></br>Odstraněna sociální síť <br></br>Přidány osobní detaily <br></br>Odstraněny osobní detaily<br></br> |
| Změněná pole (msdyn_changedfields) | Výpis objektu JSON změnil pole, nemusí ukládat hodnoty pro všechna pole.<br></br><br></br>Pro změny spočívající ve vytvoření nebo aktualizaci budou uvedena pole na vytvořeném nebo změněném záznamu.<br></br><br></br>U typů změny Přidáno se zobrazí seznam polí na podřízeném záznamu.<br></br><br></br>**Příklad:**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": true } <br></br>} |
|Historie žádosti o práci | Žádost o práci (msdyn_JobapplicatonId)<br></br>Stav (msdyn_status) <br></br>Důvod stavu (msdyn_statusreason) <br></br>Důvod zamítnutí (msdyn_rejectionreason) |
| Historie otevřené pracovní pozice | Otevřená pracovní pozice (msdyn_JobopeningId) <br></br>Stav (msdyn_jobopeningstatus) <br></br>Důvod stavu (msdyn_jobopeningstatusreason) |
| Historie kandidáta | Kandidát (msdyn_CandidateId) |
