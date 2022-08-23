---
title: Poradce při potížích s počáteční instalací
description: Tento článek obsahuje informace, které vám mohou pomoci vyřešit problémy, které mohou nastat při počátečním nastavení integrace dvojího zápisu.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d33fc6f4895b53f16cc6957a3a2fc6b1abe90a2f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289507"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Poradce při potížích s počáteční instalací

[!include [banner](../../includes/banner.md)]

Tento článek obsahuje informace o odstraňování potíží pro integrací dvojitého zápisu mezi finančními a provozními aplikacemi a Dataverse. Konkrétně obsahuje informace, které vám mohou pomoci vyřešit problémy, které mohou nastat při počátečním nastavení integrace dvojího zápisu.

> [!IMPORTANT]
> Některé problémy, které tento článek řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Nemůžete propojit finanční a provozní aplikaci do Dataverse

**Požadovaná role pro nastavení dvojitého zápisu**: Správce systému v finančních a provozních aplikacích a prostředí Dataverse.

Chyby na stránce **Nastavení odkazu na Dataverse** jsou obvykle způsobeny neúplnými problémy s nastavením nebo oprávněními. Zajistěte, aby celá kontrola stavu prošla na stránce **Nastavení odkazu na Dataverse**, jak je znázorněno na následujícím obrázku. Nemůžete propojit dvojí zapisování, pokud celý stav nepřechází na kontrolu stavu.

![Úspěšná kontrola stavu.](media/health_check.png)

Musíte mít pověření správce klienta Azure AD, chcete-li propojit prostředí financí a provozu a Dataverse. Po propojení prostředí se uživatelé mohou přihlásit pomocí svých pověření účtu a aktualizovat existující mapu tabulek.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Najít limit počtu právnických osob nebo společností, které lze propojit s dvojím zapisováním

Při pokusu o povolení map se může zobrazit následující chybová zpráva:

*Chyba dvojího zápisu – registrace modulu plug-in se nezdařila: [(nelze získat mapu oddílu pro projekt DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Chyba překračuje maximální počet povolených oddílů pro mapování DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)]. Došlo k jedné nebo více chybám.*

Aktuální limit při propojení prostředí je přibližně 40 právnických osob. K této chybě dojde, pokud se pokusíte povolit mapy a mezi prostředími je propojeno více než 40 právnických osob.

## <a name="connection-set-failed-while-linking-environment"></a>Při propojování prostředí se sada připojení nezdařila

Při propojení prostředí se duálním zápisem se akce nezdaří s chybovou zprávou:

*Uložení sady připojení se nezdařilo! Položka se stejným klíčem již byla přidána.*

Duální zápis nepodporuje více právnických osob/společností se stejným názvem. Pokud máte například dvě společnosti s názvem „DAT“ v Dataverse, pak se zobrazí tato chybová zpráva.

Chcete-li zákazníka odblokovat, odeberte duplicitní záznamy z tabulky **cdm_company** v Dataverse. Také, pokud tabulka **cdm_company** obsahuje záznamy s prázdným názvem, odeberte nebo opravte tyto záznamy.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Chyba při otevírání stránky dvojitého zápisu v finančních a provozních aplikacích

Při pokusu o propojení prostředí Dataverse pro duální zápis se může zobrazit následující chybová zpráva:

*Stavový kód odpovědi neoznačuje úspěch: 404 (Nenalezeno).*

K této chybě dojde v případě, že nedojde k dokončení kroku souhlasu aplikace. Pokud byl souhlas poskytnut, můžete ověřit přihlášením k `portal.azure.com` pomocí účtu správce klienta a kontrolou, zda se aplikace třetí strany s ID `33976c19-1db5-4c02-810e-c243db79efde` zobrazí v seznamu podnikových aplikací AAD. Pokud ne, spusťte znovu krok souhlasu, jak je popsáno v další části.

### <a name="providing-app-consent"></a>Poskytnutí souhlasu aplikace

+ Spusťte následující adresu URL pomocí vašich pověření správce.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Vyberte **Přijmout** pro souhlas. Poskytujete souhlas s instalací aplikace (s `id=33976c19-1db5-4c02-810e-c243db79efde`) ve vašem klientovi.
+ Tato aplikace je vyžadována pro komunikaci Dataverse s finančními a provozními aplikacemi.

    ![Poradce při potížích s počáteční instalací](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Pokud to nefunguje, spusťte URL v soukromém režimu Microsoft Edge nebo inkognito režimu Chrome.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Prostředí financí a provozu není zjistitelné

Může se zobrazit následující chybová zpráva:

*Prostředí finančních a provozních aplikací \*\*\*.cloudax.dynamics.com nelze zjistit.*

Existují dvě věci, které mohou způsobit problém s tím, že prostředí nelze zjistit:

+ Uživatel použitý pro přihlášení není ve stejném klientovi jako instance financí a provozu.
+ Existují určité starší instance financí a provozu hostované společností Microsoft, které měly problém se zjišťováním. Chcete-li to opravit, aktualizujte instanci financí a provozu. Prostředí se stane zjistitelným po každé aktualizaci.

## <a name="403-forbidden-error-while-connections-are-being-created"></a>Chyba 403 (Zakázáno) při vytváření připojení

V rámci procesu propojení s duálním zápisem jsou vytvořena dvě připojení Power Apps (také označovaná jako připojení *Apihub*) jménem uživatele v propojeném prostředí Dataverse. Pokud zákazník nemá licenci pro prostředí Power Apps, vytvoření připojení ApiHub se nezdaří a zobrazí se chyba 403 (Zakázáno). Následuje příklad chybové zprávy:

> MSG=\[Nepodařilo se nastavit prostředí pro duální zápis. Podrobnosti chyby:Stavový kód odpovědi neoznačuje úspěch: 403 (Zakázáno). - Stavový kód odpovědi neoznačuje úspěch: 403 (Zakázáno)\] STACKTRACE=\[   at Microsoft.Dynamics.Integrator.ProjectManagementService.DualWrite.DualWriteConnectionSetProcessor.\<CreateDualWriteConnectionSetAsync\>d\_\_29.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\DualWrite\\DualWriteConnectionSetProcessor.cs:line 297 --- End of stack trace from previous location where exception was thrown --- at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw() at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task) at Microsoft.Dynamics.Integrator.ProjectManagementService.Controllers.DualWriteEnvironmentManagementController.\<SetupDualWriteEnvironmentAsync\>d\_\_34.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\Controllers\\DualWriteEnvironmentManagementController.cs:line 265\]

K této chybě dochází z důvodu chybějící licence Power Apps. Přiřaďte příslušnou licenci (např. Power Apps Trial 2 Plan) uživateli, aby měl uživatel oprávnění vytvářet připojení. Pro ověření licence může zákazník přejít na web [Můj účet](https://portal.office.com/account/?ref=MeControl#subscriptions) pro zobrazení licencí, které jsou aktuálně přiřazeny uživateli.

Další informace o licenci Power Apps naleznete v následujících článcích:

- [Přiřazení licencí uživatelům](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide)
- [Nákup Power Apps pro vaši organizaci](/power-platform/admin/signup-for-powerapps-admin)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

