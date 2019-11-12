---
title: Analýza závady majetku
description: V tomto tématu je vysvětlena analýza závady majetku v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43772903f6845409cb33c7f2a13a049a3e9aa208
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652395"
---
# <a name="asset-fault-analysis"></a>Analýza závady majetku

[!include [banner](../../includes/banner.md)]

 

V modulu Správa majetku můžete analyzovat registrace závad majetku s cílem získat přehled o celkovém počtu závad zaregistrovaných během určitého období. Registrace závad lze analyzovat z různých perspektiv, například se zaměřením na majetek, typy majetku, funkční místa, příznaky závad nebo typy závad.

1. Klikněte na **Správa majetku** > **Dotazy** > **Závada majetku** > **Analýza závad majetku**.

2. V dialogovém okně **Výpočet analýzy závad majetku** můžete pomocí pole **Úroveň** označit, jak detailní mají být řádky závad majetku, pokud jde o funkční místa. 

    Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky závad majetku pro funkční místo, a proto lze hodiny na řádku navýšit z funkčních míst na nižší úrovni. 
        
    Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky závad majetku na všech úrovních funkčních míst, ke kterým se vztahují.

3. Chcete-li hledání omezit, můžete vybrat konkrétní majetek, data závad, příčiny závad a nápravy závad na záložce s náhledem **Záznamy k zahrnutí**.

4. Výpočet zahájíte klepnutím na tlačítko **OK**.

5. Na kartě **Analýza závad majetku** klikněte na jedno nebo více tlačítek v podokně akcí **Seskupit podle** pro zobrazení úrovně podrobností, které chcete zobrazit. Aktivovaná tlačítka jsou zvýrazněna. Kliknutím na tlačítko jej aktivujte nebo deaktivujte.

6. Kliknutím na **Aktualizovat výpočty** zobrazíte své výběry na obrazovce. 

>[!NOTE]
>Při každé aktivaci nebo deaktivaci tlačítka **Seskupit podle** nezapomeňte kliknout na tlačítko **aktualizovat výpočty**. To je nutné, protože při přepočtu pravděpodobnosti závady se zpracovává velké množství dat.

## <a name="examples"></a>Příklad

Existuje mnoho způsobů analýzy registrací závad. Tato část uvádí pět příkladů, jak různé výběry poskytují lepší přehled a podrobnosti při analýze registrací závad majetku.

### <a name="group-by-symptoms"></a>Seskupit podle příznaků

Na níže uvedeném snímku obrazovky je vybráno pouze tlačítko **Příznak**.

- Registrace závad byly provedeny se třemi příznaky poruch: únik vzduchu, vyhořelá pojistka a ucpané zařízení.  
- Ve sloupci **Pravděpodobnost %** se všechny procentuální hodnoty sčítají až do 100%. Pravděpodobnost je založena na všech registracích **příznaku** v této analýze závad.

![Obrázek č. 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a>Seskupit podle příznaků a časového období

Na níže uvedeném snímku obrazovky se přidají **Rok** a **Měsíc**, aby se zobrazil způsob zobrazení registrace závad během vybraného období.

- Příznaky závad jsou nyní zobrazeny jako registrace za rok/měsíc.  
- Pokud do sloupce **Pravděpodobnost %** přidáte všechna procenta pro každý měsíc, přidá se až 100%. Pravděpodobnost je založena na registracích **příznaku** v této analýze závad. Máte-li v majetku velký počet řádků, ale velké procento vyčnívá na řádku, bude to indikací příznaku závady, který je třeba blíže prozkoumat a nalézt způsob, jak omezit počet registrací pro tento příznak závady.

![Obrázek č. 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a>Seskupit podle více příznaků a majetku

Kombinace majetku a typu majetku se používá jako základ pro výpočty zobrazené na třech snímcích obrazovek, což zvýší úroveň podrobností.  

Obecně tlačítka ve skupině podoken akcí **Seskupit podle data**, **Seskupit podle majetku**, **Seskupit podle funkčního místa**, stejně jako tlačítko **Závada** (ID závady) obsahují období nebo relace majetku. Tlačítka **Příznak**, **Oblast**, **Typ**, **Příčina** a **Náprava** jsou kategorizace používané ve správě závad pro analýzu registrací závad majetku a poukázání na problémové oblasti.  

**Seskupit podle příznaku, majetku a typu majetku**

Na níže uvedeném snímku obrazovky byl přidán **Majetek** a **Typ majetku**, kde jsou uvedeny další podrobnosti týkající se registrací závad.

- Příznaky závad jsou nyní rozděleny do kombinací **Majetek** / **Typ majetku** / **Příznak**.  
- Pokud do sloupce **Pravděpodobnost %** přidáte všechna procenta pro kombinaci **Majetek** / **Typ majetku** / **Příznak**, každá dosáhne 100%. Pravděpodobnost je založena na registracích **příznaku** v této analýze závad. Máte-li v majetku velký počet řádků, ale velké procento vyčnívá na řádku, bude to indikací příznaku závady, který je třeba blíže prozkoumat a nalézt způsob, jak omezit počet registrací pro tento příznak závady.

![Obrázek č. 3](media/08-controlling-and-reporting.png)

**Seskupit podle dvou příznaků, majetku a typu majetku**

Na níže uvedeném snímku obrazovky byla přidána **Oblast** k možnostem **Příznak**, **Majatek** a **Typ majetku**, kde jsou uvedeny další podrobnosti týkající se registrací závad.

- Pokud do sloupce **Pravděpodobnost %** přidáte všechna procenta pro kombinaci **Majetek** / **Typ majetku** / **Příznak** na majetku, každá dosáhne 100%. Pravděpodobnost je založena na kombinaci **příznaku** a **oblasti** v této analýze závad. Máte-li v majetku velký počet řádků, ale velké procento vyčnívá na řádku, bude to indikací oblasti závady, kterou je třeba blíže prozkoumat a nalézt způsob, jak omezit počet registrací pro tuto oblast závady.  

![Obrázek č. 4](media/09-controlling-and-reporting.png)

**Seskupit podle tří příznaků, majetku a typu majetku**

Na snímku obrazovky níže byl přidán **Typ** a v tomto příkladu je zobrazen nejpřesnější výpočet.
 
- Pokud do sloupce **Pravděpodobnost %** přidáte všechna procenta pro kombinaci **Majetek** / **Typ majetku** / **Příznak** na majetku, každá dosáhne 100%. Pravděpodobnost je založena na kombinaci **příznaku**, **oblasti** a **typu** v této analýze závad. Máte-li v majetku velký počet řádků, ale velké procento vyčnívá na řádku, bude to indikací typu závady, který je třeba blíže prozkoumat a nalézt způsob, jak omezit počet registrací pro tenti typ závady.

![Obrázek č. 5](media/10-controlling-and-reporting.png)


>[!NOTE]
>Pro získání přehledu všech registrací závad vytvořených v pracovních příkazech a požadavcích na údržbu klikněte na **Správa majetku** > **Dotazy** > **Závada majetku** > **Závady majetku**. Na stránce **Závady majetku** vyberte registraci závad majetku a rozbalte podokno **Související informace**, abyste viděli informace týkající se souvisejícího pracovního příkazu nebo požadavku na údržbu.

