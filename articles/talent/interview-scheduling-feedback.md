---
title: Plánování pohovoru a zpětná vazba
description: Toto téma poskytuje informace o plánování pohovoru a aktivitách zpětné vazby v aplikaci Attract.
author: ''
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: hasrivas
ms.openlocfilehash: 7bc5a66bb221cb0ab2c69fcb1013ed48a7c664a6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2019
ms.locfileid: "374863"
---
# <a name="interview-scheduling-and-feedback"></a>Plánování pohovoru a zpětná vazba

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a>Aktivita plánovače

Aktivita plánovače je volitelná a má dvě složky: požadavek na dostupnost kandidáta a plán. Dostupnost komponenty Uchazeč umožňuje používat e-mail k vyžádání dostupnosti uchazeče. Komponenta Plán umožňuje plánování pohovorů s uchazečem a týmem náboru.

### <a name="candidate-availability-request"></a>Požadavek na dostupnost kandidáta

Pokud chcete odeslat kandidátům e-mail s dotazem na jejich dostupnost, zvolte pole **Vyžádat dostupnost kandidáta**. Pokud není toto pole zvoleno, tento krok se v procesu náboru na pracovní pozici nezobrazí.

Chcete-li odeslat požadavek na dostupnost, klikněte na **Odeslat požadavek**, vyberte dostupná data a e-mailovou šablonu a poté odešlete e-mail kandidátovi.

[![Zobrazení náborového pracovníka v aplikaci Attract pro odeslání požadavku na dostupnost kandidáta](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)

Když kandidát obdrží e-mail, aby odpověděl na požadavek, může se přihlásit na svůj kandidátský portál, vybrat data, která odpovídají jeho dostupnosti a kliknout na **Odeslat**.

### <a name="schedule"></a>Plán
Existuje několik konfigurací, které jsou k dispozici pro plánovač pohovoru pro použití a rychlé vytvoření a odeslání cyklu pohovorů tazatelům a kandidátovi.

1. Klikněte na **Vytvořit plán**a v poli **Přidat tazatele** uveďte všechny tazatele, kteří budou součástí cyklu pohovoru.
[![Zobrazení náborového pracovníka v aplikaci Attract pro zahájení plánování cyklu pohovoru](./media/schedule-start-over.png)](./media/schedule-start-over.png)   
    Pokud kandidát odpověděl na požadavek na dostupnost k pohovoru, pole **Datum pohovoru** bude předvyplněno s jeho výběrem. V případě potřeby můžete vybrat jiné datum.
    
    Pokud zvolíte pole **Změnit na panelový pohovor**, skupina tazatelů na levé straně se přesune do jednoho cyklu panelu pro vytvoření pohovoru. Potom je třeba definovat specifickou posloupnost pro pohovory.
    
    Plán pohovoru by měl být uspořádán tak, aby co nejlépe odpovídal dostupnosti účastníků. Pokud se jedná o interního kandidáta, je možné zahrnout jeho dostupnost jako součást doporučení plánu.
    
    Chcete-li mít online schůzku, zvolte pole **Přidat schůzky v aplikaci Skype** a každá událost pohovoru bude mít k dispozici odkaz na **Skype pro firmy**.

2. Vyberte trvání pohovoru pro každou událost pohovoru a klikněte na tlačítko **OK** pro zahájení vytváření plánu.

    Pokud zvolíte **Doporučení**, budou zobrazeny návrhy a mřížka pohovoru bude předvyplněná. Budete moci zobrazit aktuální dostupnost kalendáře všech zvolených tazatelů. Také budete moci zobrazit kalendář kandidáta, pokud se jedná o interního kandidáta.

3. Pokud nejsou k dispozici žádné návrhy, klikněte v sloupci **Tazatelé** na časový úsek, zadejte název pohovoru, podrobnosti a vyplňte podrobnosti o místě v případě potřeby. Můžete zahrnout odkaz na **Skype pro firmy** pro pohovor.

4. Chcete-li zahrnout další tazatele, klikněte na sloupec mřížky **Přidat pohovor** a zvolte jednoho nebo více tazatelů. Můžete použít možnost s třemi tečkami (...) pro odstraněné pohovoru z cyklu.
    
5. Pokud jsou pohovory naplánovány v jiné časové zóně, z rozbalovacího seznamu v pravém horním rohu vyberte požadované pásmo času nebo města. Mřížka dostupnosti tazatele se aktualizuje podle nového časového pásma. Tento výběr časového pásma se nyní zobrazí v zobrazení **Souhrn pohovoru**, které bude sdíleno s tazateli a kandidátem. 

6. Klikněte na **Odeslat tazatelům**, čímž odešlete zapojeným tazatelům pozvání na schůzku.

    Poté, co byly požadavky na pohovor zaslány tazatelům, ti mohou odpovědět přímo z e-mailové pozvánky, kterou dostali.

    >[!NOTE]
    > Pro všechny pohovory 1:1 jsou připomenutí odesílána tazatelům každých 24 hodin, pokud nereagoval (přejetí nebo zamítnutí) na žádost o pohovor.

    > Pro všechny panelové pohovory nejsou žádná automatizovaná připomenutí pro požadavek na pohovor. Pokud chcete připomenutí spustit ručně, upravte pohovor a použijte možnost **aktualizovat a odeslat** k odeslání žádosti zpět tazatelům.

    Odpovědi tazatele jsou zaznamenány a zobrazeny v aplikaci Attract. Pokud tazatel odmítne pozvánku, bude vám odesláno oznámení, abyste mohli provést změnu. Chcete-li zobrazit jeho odpověď v zobrazení mřížky **Plánovač**, klikněte na ikonu bubliny.

[![Zobrazení náborového pracovníka v aplikaci Attract znázorňující odpověď tazatele](./media/schedule-interviewer-response.png)](./media/schedule-interviewer-response.png)

7. Poté, co je plán pohovoru připraven ke sdílení s kandidátem, klikněte na **Odeslat kandidátovi**. Je možné zobrazit nebo skrýt jména tazatelů a časové úseky pro kandidáta.

8. Zvolte e-mailovou šablonu a odešlete souhrn pohovoru kandidátovi. Tyto informace může kandidát zobrazit ve svém e-mailu, nebo na svém portálu kandidáta.
    
>[!NOTE] 
> Dostupnost kalendáře kandidáta se zobrazí pouze tehdy, pokud je kandidát interní. Podobně pouze interní kandidáti mohou být použiti k vylepšení doporučení plánu pohovoru. V současné době kandidáti (externí nebo interní) neobdrží e-mailovou pozvánku na schůzku. Místo toho kandidát dostane pouze souhrn pohovorů.

## <a name="feedback-activity"></a>Aktivita zpětné vazby

Aktivita zpětné vazby je volitelná v šabloně práce. Tato aktivita umožňuje účastníkům pohovoru zadat doporučení nebo komentáře zpětné vazby pro uchazeče. Pokud zvolíte pole **Zdědit účastníky zpětné od náborového týmu**, budou do aktivity zpětné vazby automaticky zadáni náborář, manažer náboru a vedoucí pohovoru. Organizace mohou tazatelům povolit zobrazení zpětné vazby ostatních předtím, než odešlou vlastní zpětnou vazbu. Organizace může také povolit tazatelům úpravu zpětné vazby po odeslání. Tazatelům se připomíná, že mají odeslat zpětnou vazbu k pohovorům, které nedávno vedli, na základě přednastavené konfigurace jako součásti šablony práce. Náborový manažer nebo náborový pracovník si mohou rovněž zvolit ruční připomenutí tazateli k odeslání zpětné vazby.

## <a name="interview-activity"></a>Aktivita pohovoru

Aktivita pohovoru je volitelnou aktivitou s třemi složkami: požadavek na dostupnost kandidáta, plán a zpětná vazba. Použije aktivitu pohovoru v šabloně práce, pokud chcete všechny požadavky na dostupnost kandidáta, plány a zpětnou vazbu jako součást procesu namísto samostatného použití jako součást náborového procesu.
