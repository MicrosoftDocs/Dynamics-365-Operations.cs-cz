---
title: Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (26. března 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 568a16a17ed3269c7b72f27f0d4b7bbdbd56630e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517549"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-26-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (26. března 2019)

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

### <a name="enhancements-to-interview-scheduling"></a>Vylepšení plánování pohovoru
Následující vylepšení jsou k dispozici v plánování pohovoru.

- Náboroví manažeři nebo náboroví pracovníci nyní mohou spustit ruční připomenutí tazateli k odeslání zpětné vazby. Také lze nakonfigurovat přidruženou e-mailovou šablonu pro připomenutí.
- Při sdílení souhrnu pohovoru s kandidátem může plánovač pohovoru skrýt jména tazatelů a také skrýt řádky ze souhrnu pohovoru.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

### <a name="embedded-images-in-activities"></a>Obrázky vložené do aktivit
Nyní můžete vložit obrázky přímo do aktivit. Kromě toho, že můžete kopírovat a vkládat obrázky z webu, můžete nahrát obrázky z místního systému souborů. Velikost aktivity je omezena na 1 MB. Pokud je obrázek příliš velký, změňte jeho velikost a odešlete ho znovu.

[![Mapování](./media/embedimages.png)](./media/embedimages.png)

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR
**Sestavení 8.1.2210**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>Podpora vlastních polí pro vybrané entity ve službě Common Data Service 

Následující entity Common Data Service nyní podporují vlastní pole vytvořená v Dynamics 365 for Talent:

- Pracovník
- Etnický původ
- Statut veterána
- Kód jazyka
- Pozice
- Typ úlohy
- Pracovní funkce
- Pozice
- Typ pozice
 
### <a name="employment-history-not-displayed-chronologically"></a>Historie zaměstnance se nezobrazí chronologicky
S touto změnou nyní stránka historie zaměstnání zobrazuje záznamy o zaměstnání chronologicky, nezávisle na společnosti. Můžete také použít možnosti třídění k řazení podle společnosti.

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>Plány fixní kompenzace se nezobrazují při omezení uživatele podle společnosti v oblasti zabezpečení.
V této verzi se plány fixní kompenzace nyní zobrazují při omezení uživatelů podle společnosti v oblasti zabezpečení. Všechna nastavení zabezpečení budou respektována a pro tyto společnosti, ke kterým má uživatel oprávnění přístupu, se zobrazí fixní plány. 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>V aplikaci Talent nelze odstranit záznamy o práci pomocí možnosti Otevřít v aplikaci Excel
V této verzi můžete nyní odstranit záznamy o práci pomocí možnosti **Otevřít v aplikaci Excel** v aplikaci Dynamics 365 for Talent.

### <a name="upgrade-to-common-data-service"></a>Upgrade na Common Data Service
Konečné termíny pro upgrade na Common Data Service se rychle blíží. Přihlaste se do centra pro správu PowerApps k určení, zda je třeba provést upgrade databáze. Další informace o konečných termínech a nutných krocích k upgradu naleznete v tématu [Upgrade na Common Data Service](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Náhled

Informace o povolení funkcí náhledu naleznete v části [Přístup k funkcím náhledu v aplikaci Talent](./access-preview-feature.md).

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Povolení určení kódů důvodů na typech pracovního volna
Organizace mohou potřebovat další informace týkající se požadavků na pracovní volno. Chcete-li získat tyto informace, je třeba, aby zaměstnanci zahrnuli do svých požadavků na pracovní čas kód důvodu. V této verzi můžete nyní určit kódy důvodu přidružené k danému typu pracovního volna a umožnit zaměstnancům vybrat kód důvodu v jejich požadavcích na volno.

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>Konfigurace kódů důvod, které je třeba určit při odesílání volna pro určité typy pracovního volna
Organizace mohou vyžadovat, aby byly kódy důvodu nastaveny na konkrétních typech pracovního volna, když o něj zaměstnanci žádají. To může být vyžadováno na základě právních požadavků v jejich zemi/oblasti nebo na základě zásad společnosti. Tato verze umožňuje oddělení lidských zdrojů určit, jaké typy pracovního volna vyžadují kód důvodu. Vyplnění bude povinné, když zaměstnanci odesílají žádost o volno, které vyžaduje kód příčiny.

## <a name="coming-soon"></a>Již brzy

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Rozšířené zabezpečení kompenzace (fixní a variabilní)
V mnoha organizacích mohou mít manažeři kompenzací a zaměstnaneckých výhod přístup pouze k určitým záznamům o kompenzacích. Tyto záznamy mohou být pro vedoucí pracovníky nebo regionální zaměstnance. Díky této změně může oddělení lidských zdrojů spravovat a udržovat plány kompenzace pro různé skupiny zaměstnanců v organizaci. Fixním a variabilním plánům lze přiřadit role zabezpečení, které určí přístup k plánům a údajům zaměstnance souvisejících s plány, jako jsou například záznamy o mzdě nebo bonusech. Kompenzace pro tyto zaměstnance mohou zpracovávat pouze role, kterým byl udělen přístup.

###  <a name="email-support-for-alerts"></a>Podpora e-mailu pro výstrahy
S aktualizací Platform Update 25 mohou uživatelé vytvářet pravidla výstrah, která automaticky odesílají e-mailová oznámení kontaktům, pokud jsou spuštěny událostí. 

### <a name="duplicate-employee-checks-user-interface-changes"></a>Kontrola duplicitních zaměstnanců: změny uživatelského rozhraní
S touto změnou se při zadávání polí názvů zjistí duplicity a stav zobrazí počet nalezených duplicit. Chcete-li otevřít novou stránku, můžete vybrat poskytnutý odkaz a vyhodnotit, zda chcete použít detekovanou shodu. Aby nedošlo k přerušení zadávání dat, formulář duplicit se neotevře automaticky.
