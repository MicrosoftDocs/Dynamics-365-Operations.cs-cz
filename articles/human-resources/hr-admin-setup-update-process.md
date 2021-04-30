---
title: Aktualizace procesu
description: Microsoft Dynamics 365 Human Resources je skutečný software poskytovaný jako služba (SaaS), který poskytuje průběžné a automatické aktualizace při změnách aplikací a platforem.
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ca8868069fca4453efbb76694702a554da6d7aa6
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892268"
---
# <a name="update-process"></a>Aktualizace procesu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources je skutečný software poskytovaný jako služba (SaaS), který poskytuje průběžné a automatické aktualizace. Tyto aktualizace zahrnují změny aplikace i platformy, které často poskytují klíčová vylepšení služby, včetně pravidelných aktualizací.

## <a name="update-policy"></a>Zásady aktualizace

Aktualizace jsou vydávány v pravidelných intervalech pro všechna prostředí. Aplikace Human Resources je podporována podle [Zásad životního cyklu společnosti Microsoft](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), které poskytují konzistentní a předpověditelné pokyny pro dostupnost podpory.

## <a name="release-cadence"></a>Interval vydávání 

Aktualizace aplikace Human Resources se automaticky použijí na všechna prostředí. Aplikace Human Resources poskytuje dva typy vydání:

- **Aktualizace služeb**: Dvoutýdenní aktualizace, které zahrnují opravy chyb a nové funkce. Aktualizace služeb také zahrnují platné aktualizace platformy při jejich vydání. Chcete-li získat představu o tom, kdy jsou aktualizace platformy vydávány, viz [Tabulku 3: Vydání platformy](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases). Čtrnáctidenní intervaly aktualizace mají průběžné globální zavedení mezi oblastmi. Další informace o čtrnáctidenních aktualizacích viz [Co je nového a co se změnilo v produktu Dynamics 365 Human Resources](hr-admin-whats-new.md).

    Všechna podporovaná datacentra se aktualizují každé dva týdny, není-li uvedeno jinak. Do čtrnáctidenních aktualizací jsou zahrnuty USA, Austrálie, Evropa, Spojené království, Asie a Kanada. 

- **Aktualizace řešení Dataverse**: Tyto aktualizace se uskutečňují podle potřeby, přibližně jednou za šest týdnů. Zahrnují nové entity a změny existujících entit ve službě Dataverse. Tyto aktualizace jsou vydávány pro stejné regiony jako čtrnáctidenní aktualizace a jejich replikace do všech datacenter trvá přibližně šest týdnů. Aktualizace řešení mohou nebo nemusí být vydávány současně s čtrnáctidenními aktualizacemi služeb.

> [!NOTE]
> Aktualizace řešení jsou po vydání k dispozici ve všech datacentrech. Pokud nechcete čekat na automatickou replikaci aktualizací, můžete tyto aktualizace provést ručně v jakémkoli prostředí, v libovolném datacentru.

V případě potřeby poskytuje aplikace Human Resources také následující typy oprav:

- **Revize (oprava hotfix)**: opravy chyb, které mohou být provedeny buďto současně s vydáním čtrnáctidenní aktualizace služby, nebo odděleně

- **Nouzová oprava**: opravy hotfix prováděné preventivně a v reakci na problém, které jsou svojí povahou samostatné, mohou zahrnovat pouze změny konfigurace nebo změny kódu pro odstranění aktuálních problémů a mohou být prováděny odděleně od vydání čtrnáctidenní aktualizace služby

Vydání jsou kontrolována, testována a ověřována v interním prostředí. Po schválení jsou sestavení nasazena do výroby.

## <a name="release-cadence-exceptions-in-2021"></a>Uvolnit výjimky frekvence v 2021

Kvůli svátkům je plán vydání pro listopad a prosinec 2021 následující:

- Vydání v listopadu: 1. listopadu – 14. listopadu
- Vydání v prosinci: 29. listopadu – 12. prosince
 
Kadence dvoutýdenního vydání bude obnovena jako obvykle 10. ledna 2022.

## <a name="communications"></a>Sdělení

Zde uvádíme, co bylo provedeno v případě aplikace Human Resources a co jsme vydali v následujících místech:

- [Dynamics 365 Human Resources plán](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Plány vydání Dynamics 365](/dynamics365/release-plans/)

- [Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Hledání problémů ve službě Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (pouze chyby týkající se platformy)

- [Blog aplikace Human Resources](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Komunita aplikace Human Resources v síti Yammer](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Ověření předběžných verzí funkcí v izolovaném testovacím prostředí (sandbox)

Předběžnou verzi funkcí můžete ověřit v izolovaném testovacím prostředí předtím, než ji povolíte ve svém produkčním prostředí. Další informace o povolování funkcí naleznete v tématu [Přehled správy funkcí](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Všechny nové funkce zůstanou v náhledu nejméně 30 dnů a obvykle jsou zde 30-60 dní. Hlavní funkce jsou obvykle k dispozici v říjnu a dubnu každého roku po období náhledu. Jakmile se v pracovním prostoru Správa funkcí zobrazí nové funkce, můžete je zapnout. Některé funkce mohou být ve výchozím nastavení zapnuty.

V některých případech bude ve výchozím nastavení zapnuta integrální funkce a nelze ji vypnout (například pracovní prostor Správa funkcí).

Jakmile je funkce obecně k dispozici, může být zapnuta nebo vypnuta v provozních prostředích. Pracovní prostor Správa funkcí označuje, kdy bude funkce náhledu povinná. Toto datum je obvykle 1. října nebo 1. ledna, aby bylo možné vyrovnat je s pololetními plány vydávání. Nemůžete zapínat a vypínat povinné funkce. Dokud nebude povinná, můžete funkci zapnout nebo vypnout ve všech prostředích.

Důrazně doporučujeme ověřovat funkce v izolovaném testovacím prostředí nebo ve zkušebním prostředí. Nejlepším řešením je vytvořit kopii vašeho aktuálního produkčního prostředí nebo databáze v izolovaném testovacím prostředí (sandbox), tak abyste mohli kompletně vyzkoušet nové funkce na svých datech.

Další informace o zřizování izolovaného testovacího prostředí naleznete v tématu [Zřízení projektu aplikace Human Resources](hr-admin-setup-provision.md). Informace o odebrání testovacího prostředí naleznete v tématu [Odebrání instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Hlášení chyb

Při testování předběžných verzí funkcí nebo při zkoušení nových funkcí můžete zjistit, že některé položky nefungují dle očekávání. Veškeré chyby nahlaste prostřednictvím [podpory služby Microsoft Dynamics 365](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Viz také

[Služba Dynamics 365 a plány vydání Power Platform](/dynamics365/release-plans)</br>
[Co je nového nebo co se změnilo v aplikaci Human Resource služby Dynamics 365](hr-admin-whats-new.md)</br>
[Zásady životního cyklu softwaru](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]