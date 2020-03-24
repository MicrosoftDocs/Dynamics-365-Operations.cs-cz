---
title: Aktualizace procesu
description: Microsoft Dynamics 365 Human Resources je skutečný software poskytovaný jako služba (SaaS), který poskytuje průběžné a automatické aktualizace při změnách aplikací a platforem.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 267682f4497bacf70f93840a948d0e525dfa4aa1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092194"
---
# <a name="update-process"></a>Aktualizace procesu

Microsoft Dynamics 365 Human Resources je skutečný software poskytovaný jako služba (SaaS), který poskytuje průběžné a automatické aktualizace. Tyto aktualizace zahrnují změny aplikace i platformy, které často poskytují klíčová vylepšení služby, včetně pravidelných aktualizací.

## <a name="update-policy"></a>Zásady aktualizace

Aktualizace jsou vydávány v pravidelných intervalech pro všechna prostředí. Aplikace Human Resources je podporována podle [Zásad životního cyklu společnosti Microsoft](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), které poskytují konzistentní a předpověditelné pokyny pro dostupnost podpory.

## <a name="release-cadence"></a>Interval vydávání

Aktualizace aplikace Human Resources se automaticky použijí na všechna prostředí. Aplikace Human Resources poskytuje dva typy vydání:

- **Aktualizace služeb**: Týdenní aktualizace, které zahrnují opravy chyb a nové funkce. Aktualizace služeb také zahrnují platné aktualizace platformy při jejich vydání. Chcete-li získat představu o tom, kdy jsou aktualizace platformy vydávány, viz [Tabulku 3: Vydání platformy](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases). Týdenní aktualizace jsou obvykle vydávány ve středu. Další informace o týdenních aktualizacích viz [Co je nového a co se změnilo v produktu Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).

    Všechna podporovaná datacentra se aktualizují týdně, není-li uvedeno jinak. Týdenní aktualizace obvykle začínají ve středu a jsou dokončeny do neděle. Do týdenních aktualizací jsou zahrnuty USA, Austrálie, Evropa, Spojené království, Asie a Kanada. 

- **Aktualizace řešení Common Data Service**: Tyto aktualizace se uskutečňují podle potřeby, přibližně jednou za šest týdnů. Zahrnují nové entity a změny existujících entit ve službě Common Data Service. Tyto aktualizace jsou vydávány pro stejné regiony jako týdenní aktualizace a jejich replikace do všech datacenter trvá přibližně šest týdnů. Aktualizace řešení mohou nebo nemusí být vydávány současně s týdenními aktualizacemi služeb.

V následující tabulce je uvedena ukázka plánu:

| Týden | Typ aktualizace |
| --- | --- |
| 1 | Aktualizace služby (všechny regiony) |
| 2 | Aktualizace služby (všechny regiony) + aktualizace řešení (regiony pro týden č. 1) |
| 3 | Aktualizace služby (všechny regiony) + aktualizace řešení (regiony pro týden č. 2) |
| 4 | Aktualizace služby (všechny regiony) + aktualizace řešení (regiony pro týden č. 3) |
| 5 | Aktualizace služby (všechny regiony) + aktualizace řešení (regiony pro týden č. 4) |
| 6 | Aktualizace služby (všechny regiony) + aktualizace řešení (regiony pro týden č. 5) |
| 7 | Aktualizace služby (všechny regiony) + aktualizace řešení (regiony pro týden č. 6) |
| 8 | Aktualizace služby (všechny regiony) |

> [!NOTE]
> Aktualizace řešení jsou po vydání k dispozici ve všech datacentrech. Pokud nechcete čekat na automatickou replikaci aktualizací, můžete tyto aktualizace provést ručně v jakémkoli prostředí, v libovolném datacentru.

V případě potřeby poskytuje aplikace Human Resources také následující typy oprav:

- **Revize (oprava hotfix)**: opravy chyb, které mohou být provedeny buďto současně s vydáním týdenní aktualizace služby, nebo odděleně

- **Nouzová oprava**: opravy hotfix prováděné preventivně a v reakci na problém, které jsou svojí povahou samostatné, mohou zahrnovat pouze změny konfigurace nebo změny kódu pro odstranění aktuálních problémů a mohou být prováděny odděleně od vydání týdenní aktualizace služby

Vydání jsou kontrolována, testována a ověřována v interním prostředí. Po schválení jsou sestavení nasazena do výroby.

## <a name="exceptions-in-2019"></a>Výjimky v roce 2019

Následující data představují výjimky z plánu pravidelných vydání:

| Datum | Popis |
| --- | --- |
| Týden zahrnující 25. listopad | Žádné aktualizace |
| Týden zahrnující 16. prosinec | Pouze menší aktualizace |
| Týden zahrnující 23. prosinec | Žádné aktualizace |
| Týden zahrnující 30. prosinec | Žádné aktualizace |

## <a name="communications"></a>Sdělení

Zde uvádíme, co bylo provedeno v případě aplikace Human Resources a co jsme vydali v následujících místech:

- [Dynamics 365 Human Resources plán](https://dynamics.microsoft.com/roadmap/talent/)

- [Plány vydání Dynamics 365](https://docs.microsoft.com/dynamics365/release-plans/)

- [Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Hledání problémů ve službě Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (pouze chyby týkající se platformy)

- [Blog aplikace Human Resources](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Komunita aplikace Human Resources v síti Yammer](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Ověření předběžných verzí funkcí v izolovaném testovacím prostředí (sandbox)

Předběžnou verzi funkcí můžete ověřit v izolovaném testovacím prostředí předtím, než ji povolíte ve svém produkčním prostředí. Další informace o povolování funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Všechny nové funkce zůstanou v náhledu nejméně 30 dnů a obvykle jsou zde 30-60 dní. Hlavní funkce jsou obvykle k dispozici v říjnu a dubnu každého roku po období náhledu. Jakmile se v pracovním prostoru Správa funkcí zobrazí nové funkce, můžete je zapnout. Některé funkce mohou být ve výchozím nastavení zapnuty.

V některých případech bude ve výchozím nastavení zapnuta integrální funkce a nelze ji vypnout (například pracovní prostor Správa funkcí).

Jakmile je funkce obecně k dispozici, může být zapnuta nebo vypnuta v provozních prostředích. Pracovní prostor Správa funkcí označuje, kdy bude funkce náhledu povinná. Toto datum je obvykle 1. října nebo 1. ledna, aby bylo možné vyrovnat je s pololetními plány vydávání. Nemůžete zapínat a vypínat povinné funkce. Dokud nebude povinná, můžete funkci zapnout nebo vypnout ve všech prostředích.

Důrazně doporučujeme ověřovat funkce v izolovaném testovacím prostředí nebo ve zkušebním prostředí. Nejlepším řešením je vytvořit kopii vašeho aktuálního produkčního prostředí nebo databáze v izolovaném testovacím prostředí (sandbox), tak abyste mohli kompletně vyzkoušet nové funkce na svých datech.

Další informace o zřizování izolovaného testovacího prostředí naleznete v tématu [Zřízení projektu aplikace Human Resources](hr-admin-setup-provision.md). Informace o odebrání testovacího prostředí naleznete v tématu [Odebrání instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Hlášení chyb

Při testování předběžných verzí funkcí nebo při zkoušení nových funkcí můžete zjistit, že některé položky nefungují dle očekávání. Veškeré chyby nahlaste prostřednictvím [podpory služby Microsoft Dynamics 365](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Viz také

- [Služba Dynamics 365 a plány vydání Power Platform](https://docs.microsoft.com/dynamics365/release-plans)
- [Co je nového nebo co se změnilo v aplikaci Human Resource služby Dynamics 365](hr-admin-whats-new.md)
- [Zásady životního cyklu softwaru](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

