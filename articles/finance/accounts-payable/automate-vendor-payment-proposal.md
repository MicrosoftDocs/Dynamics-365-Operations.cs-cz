---
title: Automatizace návrhů plateb dodavatelům
description: Tohle téma vysvětluje, jak mohou organizace, které platí dodavatelům podle opakujícího se plánu, automatizovat proces generování návrhů plateb dodavatelům.
author: kweekley
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 238123f59c3d85b2b2c64aed9d94c7d8af27eaf2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820804"
---
# <a name="automate-vendor-payment-proposals"></a>Automatizace návrhů plateb dodavatelům

[!include [banner](../includes/banner.md)]

Organizace, které platí dodavatelům podle opakujícího se plánu, nyní mohou automatizovat proces generování návrhů plateb dodavatelům. Automatizace návrhů plateb dodavatelům definují následující podrobnosti:

- Kdy jsou spuštěny návrhy plateb
- Jaká kritéria se použijí pro výběr faktur, které mají být zaplaceny
- V jakém deníku plateb dodavateli jsou výsledné platby uloženy

Automatizace návrhů plateb neúčtuje platby automaticky. Proto můžete i nadále používat jakékoli procesy ověřování a pracovních postupů, které aktuálně používáte ke schvalování vytvořených plateb.

## <a name="define-the-occurrence-of-vendor-payment-proposals"></a>Definování výskyt návrhů plateb dodavatelům

Automatizace návrhů plateb dodavatelům používá systém automatizace procesů. Různé obchodní procesy používají tento systém k definování opakování vybraného procesu. V případě návrhů plateb dodavatelům je automatizace přístupná na adrese **Závazky \> Nastavení platby \> Automatizace procesů**.

Nejprve použijte možnost automatizace **Vytvořit nový proces** a vyberte **Návrh platby dodavateli**. Průvodce vás provede procesem nastavení nabídky platby dodavateli.

## <a name="general-page"></a>Stránka Obecné

Na stránce průvodce **Obecné** zadejte název návrhu platby dodavateli, který vytváříte. Pokud například platíte všem domácím dodavatelům v pondělí šekem, zadejte popisný název jako **Domácí\_Šek**. Název, který zadáte, se zobrazí v týdenním zobrazení automatizace procesů v pracovním prostoru **Platby dodavatelům**.

Dále definujte vlastníka vytvořeného deníku plateb. Vlastníkem je obvykle úředník pro platby závazků, který je zodpovědný za platební deník po jeho vytvoření.

Zbývající nastavení na stránce jsou obecná a používají se k definování vzoru výskytu pro tuto verzi návrhu platby dodavateli. Pokud je například výskyt plateb šeků v pondělí, můžete jej definovat tak, aby se spouštěl každý týden, a můžete vybrat pondělí jako den v týdnu, kdy se spustí. Můžete také zadat čas předběžného plánu, například 14:00, takže automatizace procesů bude dokončena před začátkem následujícího pracovního dne.

Je důležité, abyste pochopili, že pomocí průvodce definujete, kdy bude zpracován návrh platby dodavateli. Nedefinujete, kdy jsou platby dodavateli generovány, vytištěny a zaúčtovány. V týdenním zobrazení se automatizace procesů u návrhů plateb dodavatelům objeví ve dnech, které jsou vybrány ve vzoru výskytu.

Pro více informací o ostatních polích na stránce **Obecné** viz dokumentace k automatizaci procesů.

## <a name="vendor-payment-proposal-page"></a>Stránka návrhu platby dodavateli

Další stránka v průvodci je stránka **Návrh platby dodavateli**. Slouží k definování kritérií pro výběr faktur dodavatele, které mají být zaplaceny. Obecně platí, že stejné možnosti jsou uvedeny v návrhu platby v deníku plateb dodavateli. Existuje však několik výjimek. Například všechna data na této stránce musí být definována jako relativní data, protože datum návrhu platby se mění pokaždé, když je návrh spuštěn.

### <a name="journal-name"></a>Název deníku

Pole **Název deníku** definuje název deníku, ve kterém jsou platby dodavateli vytvořeny. Výsledky automatizace návrhu platby dodavateli vytvoří platby v definovaném deníku, ale deník není zaúčtován.

### <a name="from-date-and-to-date"></a>Datum „od“ a datum „do“

Místo definování data „od“ a data „do“ pro výběr faktur na základě data splatnosti nebo data platební slevy musíte použít volbu **Definovat kritéria „Do data“** a pole **Úprava počtu dnů „Do data“** pro definování data „do“. V automatizaci návrhů plateb neexistuje pojem data „od“.

Ve výchozím nastavení je volba **Definovat kritéria „Do data“** nastavena na **Ne**. Pokud použijete tuto výchozí hodnotu, proces při svém spuštění vyberte všechny faktury k platbě, protože nebylo definováno žádné datum „do“.

Pokud nastavíte volbu **Definovat kritéria „Do data“** na hodnotu **Ano**, použijte pole **Úprava počtu dnů „Do data“** pro definování data, kdy jsou faktury vybrány, jako zadaný počet dní před nebo po datu spuštění procesu. Číslo může být kladné, záporné nebo 0 (nula). Systém poté zaplatí faktury, kde data splatnosti nebo data platební slevy představují počet dní před nebo po datu, kdy se proces spustí. Například u všech faktur, které jsou splatné v pátek nebo před pátkem, vytvoří řada plateb platby šekem všem dodavatelům ve středu. V tomto případě nastavte pole **Úprava počtu dnů „Do data“** na **2**. Když je návrh na platbu spuštěn ve středu 25. března, budou pro platbu vybrány všechny faktury, které mají datum splatnosti nebo slevu v hotovosti do 27. března nebo dříve.

### <a name="minimum-payment-date"></a>Minimální datum platby

Minimální datum platby definuje nejbližší datum, které je použito při vytvoření plateb. Nejprve musíte nastavit volbu **Definovat kritéria minimálního data platby** na **Ano**. Toto nastavení umožňuje použít funkci minimálního data platby. Pokud tuto volbu nastavíte na hodnotu **Ano**, použijte pole **Úprava počtu dnů pro minimální datum platby** pro definování minimálního data platby jako zadaného počtu dní před nebo po datu spuštění procesu. Číslo může být kladné, záporné nebo 0 (nula). Například řada plateb generuje platby ve středu, aby zahrnovala všechny platby, které mají minimální datum splatnosti k předchozímu pondělí. V tomto případě nastavte pole **Úprava počtu dnů pro minimální datum platby** na **-2**.

Zde je příklad, který ukazuje, jak spolupracují pole pro datum „do“ a datum minimální platby. Automatizace platebních návrhů je nastavena ke spuštění ve středu. Pole **Úprava počtu dnů „Do data“** je nastaveno na **1**, takže definuje datum „do“ na základě data splatnosti. Pole **Úprava počtu dnů pro minimální datum platby** je nastaveno na **-2**. Pokud automatizace platebního procesu začne ve středu 25. března, budou do návrhu platby zahrnuty všechny faktury splatné do 26. března nebo dříve. Návrhy plateb budou generovány následujícím způsobem:

- Všechny faktury, které jsou splatné do 23. března nebo dříve, budou mít datum platby 23. března.
- Faktury, které jsou splatné do 24. března, budou mít datum platby 24. března.
- Faktury, které jsou splatné do 25. března, budou mít datum platby 25. března.
- Faktury, které jsou splatné do 26. března, budou mít datum platby 26. března.

### <a name="summarized-payment-date"></a>Datum souhrnné platby

Souhrnné datum platby se používá pouze v případě, kdy je pole **Období** pro způsob platby faktur nastaveno na hodnotu **Celkem**. Pokud je pole **Období** nastaveno na **Celkem** pro váš způsob platby, musíte nastavit možnost **Definovat kritérium souhrnného data platby** na **Ano**. Pokud tuto volbu nastavíte na hodnotu **Ano**, použijte pole **Úprava počtu dnů pro souhrnné datum platby** pro definování souhrnného data platby jako zadaného počtu dní před nebo po datu spuštění procesu. Číslo může být kladné, záporné nebo 0 (nula). Například řada generuje platby ve středu a společnost chce vytvořit souhrnnou platbu ve středu. V tomto případě nastavte pole **Úprava počtu dnů pro souhrnné datum platby** na **0**.

### <a name="records-to-include"></a>Záznamy k zahrnutí

Možnosti filtru lze pro návrh platby stále definovat. Pokud je definován filtr, kritéria filtru se na stránce průvodce nezobrazí. Lze je však zobrazit opětovným otevřením filtru.

Zbývající pole pro návrh fungují stejně jako pro návrh platby v deníku plateb dodavateli. Informace o ostatních polích viz [Vytvoření plateb dodavatelům pomocí návrhu platby](create-vendor-payments-payment-proposal.md).

> [!NOTE]
> Některá pole pro konkrétní zemi/oblast a některá pole pro veřejný sektor zatím nejsou v automatizaci návrhů plateb dodavateli k dispozici.

Doporučujeme, abyste na základě vašich požadavků vyhodnotili, zda bude automatizace přínosem pro vaši organizaci.

## <a name="view-the-results-of-a-vendor-payment-proposal-automation"></a>Zobrazení výsledků automatizace návrhu platby dodavateli

Po vytvoření řady automatizace návrhu platby dodavateli jsou výskyty pro každou platbu zobrazeny v týdenním zobrazení automatizace procesů. U plateb dodavatelům bylo do pracovního prostoru **Platby dodavatelům** a na stránku **Automatizace procesů** přidáno týdenní zobrazení automatizace procesů.

[![Týdenní zobrazení automatizace procesů v pracovním prostoru Platby dodavatelům](./media/vendor-payment-proposal-1.png)](./media/vendor-payment-proposal-1.png)

Týdenní zobrazení automatizace procesů v pracovním prostoru **Platby dodavatelům** zobrazuje pouze automatizace návrhů plateb dodavatelům. Zobrazuje všechny výskyty plateb za aktuální týden pro všechny právnické osoby, ke kterým má přihlášený uživatel bezpečnostní oprávnění. Pokud je například úředník pro platby závazků zodpovědný za platby ve společnostech USMF a USSI, uvidí výskyty automatizace návrhů plateb dodavatelům pro tyto dvě společnosti, nikoli však pro jiné společnosti.

[![Týdenní zobrazení automatizace procesů pro společnosti USMF a USSI](./media/vendor-payment-proposal-2.png)](./media/vendor-payment-proposal-2.png)

Každý výskyt zobrazuje společnost, ve které byl nebo bude vytvořen deník plateb. Pokud jsou platby vytvářeny pomocí centralizovaných plateb, zobrazí se společnost, ve které budou platby vytvořeny. Výskyt nutně neukazuje, které faktury společností budou zaplaceny.

Název každého výskytu je rovněž zobrazen, aby pomohl identifikovat návrh platby.

Dále je zobrazen stav každého výskytu. Jsou použity následující stavy:

- **Naplánováno** – Návrh platby je naplánován, ale dosud nebyl spuštěn.
- **Chyba** – Návrh platby byl spuštěn, ale došlo k chybě. Chyby si můžete prohlédnout výběrem tlačítka **Zobrazit výsledky**.
- **Dokončeno** – Návrh platby byl úspěšně spuštěn. Platby si můžete prohlédnout výběrem odkazu **Zobrazit platby**. Tento odkaz otevře deník plateb, který byl vytvořen výskytem.

Po vytvoření plateb můžete zobrazit částky plateb v deníku. Částky jsou zobrazeny v měnách transakcí. Pokud například deník plateb obsahuje platby v amerických i kanadských dolarech, zobrazí se celkové platby pro každou měnu. 

Deník plateb lze po jeho vytvoření prostřednictvím automatizace procesů odstranit. Pokud je platba zcela odstraněna, dojde k následujícím událostem:

- Automatizace procesů pro tento týden zůstává ve stavu **Dokončeno**.
- Proces odstraní součty plateb a odkaz **Zobrazit platby** je nahrazen tlačítkem **Zobrazit výsledky**.
- Při zobrazení výsledků obdržíte zprávu, která uvádí, že původní deník byl odstraněn.

Po odstranění platby budou faktury znovu otevřeny k platbě. Poté může být vytvořen nový výskyt pro opětovné zaplacení faktur.

## <a name="edit-a-vendor-payment-proposal-automation"></a>Úprava automatizace návrhu platby dodavateli

Systém automatizace procesů vám umožňuje upravit platbu, řadu a výskyty, které jsou vytvořeny pro návrh platby. Řadu lze upravit buď na stránce **Automatizace procesů** nebo v týdenním zobrazení automatizace procesů. Pokud se například správce závazků rozhodne vygenerovat všechny šeky pro domácí dodavatele ve středu místo v pondělí, může najít událost v týdenním zobrazení a vybrat **Zobrazit/Upravit – Řada**. Pokud upravíte řadu, systém vás vyzve k zadání, zda by se měla změna provést u všech existujících výskytů, nebo pouze u nových výskytů. Historické události, které již mají stav **Dokončeno** nebo skončily stavem **Chyba**, se nezmění.

Můžete také přidat nový výskyt nebo změnit existující výskyt. Například další výskyt návrhu plateb je naplánován na středu 1. ledna, ale toto datum je svátek. Výskyt můžete změnit buď z týdenního zobrazení automatizace procesů nebo na stránce **Automatizace procesů**. Otevře se stránka, která zobrazuje podrobnosti plánu a kritéria návrhu platby. Zde můžete upravit plánovaný čas a datum. V případě potřeby můžete také upravit kritéria návrhu platby. Pokud například změníte plánované datum výskytu platby z 1. ledna na 2. ledna, můžete také změnit relativní data pro datum „do“.

Můžete také zakázat výskyt nebo řadu. Chcete-li zakázat výskyt a pozastavit jeho zpracování, vyberte jej v týdenním zobrazení automatizace procesů a poté vyberte **Zakázat**. Řadu můžete zakázat na stránce **Automatizace procesů**.

## <a name="security-for-payment-proposal-automations"></a>Zabezpečení automatizací návrhů plateb

Pro automatizace návrhů plateb dodavatelům byly přidány následující povinnosti a oprávnění. Tyto povinnosti a oprávnění jsou výchozím nastavením zabezpečení, ale lze je změnit na základě požadavků vaší organizace. Například, pokud to není jen správce závazků, ale také úředník plateb závazků, kdo může upravovat a vytvářet opakování plánu, přiřaďte povinnost **Údržba výskytů v plánu** osobě v roli úředníka plateb závazků.

| Funkční oprávnění                              | Role                                                                       | Oprávnění |
|-----------------------------------|----------------------------------------------------------------------------|------------|
| Údržba řady plánu          | Manažer závazků                                                   | Tato povinnost uděluje práva vytvářet a udržovat řadu automatizace návrhů plateb a jejich výskyt prostřednictvím následujících oprávnění:<ul><li>Údržba výskytů v plánu</li><li>Údržba řady plánu</li><li>ProcessScheduleOccurrenceListMaintain</li><li>Zobrazení týdenního zobrazení výskytů</li></ul> |
| Dotaz na výskyty v plánu | Úředník pro platby závazků, úředník pro centralizované platby závazků | Tato povinnost uděluje práva zobrazovat výskyty automatizace návrhů plateb prostřednictvím následujících oprávnění:<ul><li>Zobrazení výskytů v plánu</li><li>Zobrazení týdenního zobrazení výskytů</li></ul> |
| Dotaz na řadu plánu      | Žádní                                                                       | Tato povinnost uděluje práva zobrazovat nastavení řady a výskytů prostřednictvím následujících oprávnění:<ul><li>Zobrazení výskytů v plánu</li><li>Zobrazení stránku se seznamem výskytů</li><li>Zobrazení týdenního zobrazení výskytů</li></ul>|
| Údržba výskytů v plánu     | Žádní                                                                       | Tato povinnost uděluje práva vytvářet a udržovat výskyt prostřednictvím následujících oprávnění:<ul><li>Údržba výskytů v plánu</li><li>Zobrazení týdenního zobrazení výskytů</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]