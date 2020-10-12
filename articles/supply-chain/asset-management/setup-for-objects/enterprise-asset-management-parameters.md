---
title: Parametry správy majetku
description: Ve správě majetku musí být nastaveny obecné parametry týkající se majetku, pracovních příkazů a plánování pracovních příkazů.
author: josaw1
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2505f5f334c3f86959023812880e956f0ebaac09
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889834"
---
# <a name="asset-management-parameters"></a>Parametry správy majetku

[!include [banner](../../includes/banner.md)]

Ve správě majetku musí být nastaveny obecné parametry týkající se majetku, pracovních příkazů a plánování pracovních příkazů. Toto téma vysvětluje, jak je nastavit. Vyberte **Správa majetku** > **Nastavení** > **Parametry správy majetku** pro otevření stránky.

> [!NOTE]
> Chcete-li nastavit systém obsahující ukázková data pro testování funkcí správy majetku, vyhledejte pokyny v tématu [Nasazení ukázkového prostředí](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).

Odkaz **Majetek**

- **Výchozí funkční místo** je standardní funkční místo, které je automaticky vybráno u majetku při vytváření nového majetku.  
- V poli **Standardní kalendář** vyberte kalendář, který se má použít pro výpočet ukazatelů KPI majetku v případě, že u majetku není vybrán žádný zdroj.  
- V poli **Zobrazení** vyberte standardní zobrazení, které se zobrazí při otevření **Zobrazení majetku** (**Správa majetku** > **Společné** > **Majetek** > **Zobrazení majetku**).
- **Výchozí type požadavku** je standardní typ požadavku na údržbu, který je automaticky vybrán při vytváření nového požadavku.  
- Pokud chcete vytvořit projekty, které se vztahují k majetku, vztahy projektu týkající se výběru **hlavního projektu**, **hierarchie projektu** a možnost pro **automatické vytvoření projektů** se nastavují v **parametrech správy majetku**.  
- V poli **Maska projektu pracovního příkazu** definujete počet dílčích projektů povolených pro pracovní příkazy a dílčí majetek. Maska pracovního příkazu se používá k definování počtu pracovních příkazů, které lze vytvořit na majetku a použít na souvisejícím projektu úlohy pracovního příkazu. Maska pracovního příkazu je nastavena v poli **Maska souvisejícího pracovního příkazu** v **parametrech správy majetku** (**Správa majetku** > **Nastavení** > **Parametry správy majetku** > **Pracovní příkazy**).  
    >[!NOTE]
    >Formát související masky pracovního příkazu je počet znaků hash (#) v závislosti na maximálním počtu pracovních příkazů, které chcete na majetku vytvořit. Příklad: ## umožňuje vytvořit až 99 dílčích projektů.  
- Prognózy pro typy úloh jsou uloženy v projektu vybraném v poli **Projekt prognózy**. Pro každý typ úlohy se automaticky vytvoří nová aktivita v projektu prognózy. Prognózy pro typ úlohy se pak uloží do projektu prognózy.  
- V poli **Model** vyberte model prognózy použitý pro typ práce a prognózy pracovních příkazů.  


Odkaz **Pracovní příkazy**

- **Výchozí typ pracovního příkazu** definuje standardní nastavení při vytváření pracovního příkazu.  
- **Typ preventivního pracovního příkazu** definuje typ pracovního příkazu, který se používá při vytváření pracovních příkazů z plánů údržby. Pokud je toto pole ponecháno prázdné, použije se typ pracovního příkazu v poli **Výchozí typ pracovního příkazu**.  
- V poli **Maska souvisejícího pracovního příkazu** definujete maximální počet pracovních příkazů, které mohou souviset s pracovním příkazem. Příklad: ## umožňuje použít až 99 souvisejících pracovních příkazů. Pokud definujete masku tak, jak je zde uvedeno, budou související pracovní příkazy očíslovány [ID pracovního příkazu, s nímž je spojen pracovní příkaz]-01,-02,-03 atd. Pokud v tomto poli nedefinujete masku, související pracovní příkaz dostane ID s následujícím pořadovým číslem.  
- Pokud chcete automaticky kopírovat chyby registrované na pracovních příkazech do souvisejících požadavků na údržbu, vyberte možnost **Ano** na přepínacím tlačítku **Kopírovat chyby**. 
- V poli **Úroveň** definujete úroveň funkčních míst, která je automaticky vložena do pracovního příkazu, pokud všechny související úlohy pracovních příkazů odkazují na stejné funkční místo. Pokud úlohy pracovních příkazů nesouvisí všechny se stejným funkčním místem na definované úrovni, pole **Funkční místo** zůstane na pracovním příkazu prázdné. Například: Pokud do tohoto pole vložíte číslo 1, jedná se o nejvyšší úroveň ve struktuře funkčních míst. Pokud do tohoto pole vložíte číslo 0, nedefinovali jste specifickou úroveň funkčního místa, ale pouze to, že všechny úlohy pracovních příkazů na pracovním příkazu musí souviset se stejným funkčním místem, které má být přidáno do pracovního příkazu.  
- Deníky používané při účtování spotřeby na pracovním příkazu lze vybrat na záložce s náhledem **Obecné** v polích **Hodina**, **Položka** a **Výdaje**.  
- V poli **Zdroj jazyka produktu** vyberte jazyk, který chcete použít pro názvy produktů v sestavách správy majetku. Můžete vybrat jazyk nastavený na účtu společnosti nebo jazyk nastavený pro aktuálně přihlášeného uživatele.  
- Chcete-li automaticky aktualizovat změny ve výchozích hodnotách typu práce, plánech údržby a pořadí údržby, zvolte **Ano** v **Aktualizace v reálném čase**.
  - Pokud vyberete možnost **Ne**, změny výchozího nastavení typu úlohy, plánů údržby a pořadí údržby nebudou automaticky aktualizovány v modulu Správa majetku.
  - Pokud máte velké množství synchronizovaných dat, například mnoho majetku nebo funkčních míst nastavených v plánech údržby nebo v pořadích údržby, nebo velký počet plánů nebo pořadí údržby, vyberte na přepínacím tlačítku **Ne**.  
  - Pokud provedete změny ve výchozích hodnotách typu úlohy nebo v plánech či pořadích údržby a pro aktualizaci reálného času jste zvolili **Ne**, varování se nemusí zobrazit, pokud změny ovlivňují:
    - Funkční místa nastavená na plánech nebo pořadích údržby  
    - Objekty nastavené na plánech nebo pořadích údržby  
    - Nastavení plánů údržby  
    - Nastavení pořadí údržby  
- Na záložce s náhledem **Kategorie** lze definovat výchozí kategorie týkající se spotřeby na pracovních příkazech.  


Odkaz **Plánování pracovního příkazu**

- **Ochranná doba plánu** určuje období ve dnech, vypočítané od očekávaného počátečního data pracovního příkazu, během něhož jsou plánovány úlohy pracovního příkazu.  
- **Hlavní plán** se vztahuje ke zdrojům v modulu **Správy organizace**. Pokud v tomto poli vyberete hlavní plán, budete moci zobrazit rezervace kapacity vztahující se k pracovním příkazům v možnosti **Rezervace kapacity** (**Správa organizace** > **Zdroje** > **Zdroje** > volba zdroje > karta **Zdroj** > tlačítko **Rezervace kapacity**). Pokud toto pole ponecháte prázdné, budete moci zobrazit vytížení kapacity vztahující se k pracovním příkazům v možnosti **Vytížení kapacity** (**Správa organizace** \> **Zdroje** \> **Zdroje** \> volba zdroje \> karta **Zdroj** \> tlačítko **Vytížení kapacity**).  

>[!NOTE]
>Výběr týkající se použití hlavního plánu v modulu **Správa majetku** a souvisejícího formuláře používaného k získání přehledu rezervací kapacity nebo vytížení kapacity je standardní nastavení. V závislosti na nastavení v poli **Hlavní plán** budete moci získat přístup k informacím o kapacitě buď v možnosti **Rezervace kapacity** nebo **Vytížení kapacity** v modulu **Správa organizace**. Není možné vytvořit nastavení, ve kterém jsou v obou zobrazeních zobrazeny rezervace kapacity.  

Pole popsaná v následujícím seznamu se vztahují k vypočítaným skóre hodnocení, která se používají k výpočtu priority pracovního příkazu během plánování pracovního příkazu.

- **Priorita** - skóre hodnocení vypočtené společně se skórem hodnocení v polích **Kritičnost** a **Počáteční datum**. Číslo v tomto poli je vyděleno číslem v poli **Priorita** na pracovním příkazu. Příklad: Pokud je do tohoto pole vložena hodnota 5 a pracovní příkaz má prioritu 20, skóre hodnocení priority je 0,25.  
- **Kritičnost** - skóre hodnocení vypočtené společně se skórem hodnocení v polích **Priorita** a **Počáteční datum**. Číslo v tomto poli je vynásobeno číslem v poli **Kritičnost** na pracovním příkazu. Příklad: Pokud je do tohoto pole vložena hodnota 10 a pracovní příkaz má kritičnost 5, skóre hodnocení kritičnosti je 50.  
- **Počáteční datum** - skóre hodnocení vypočtené společně se skórem hodnocení v polích **Priorita** a **Kritičnost**. Toto pole označuje denní skóre jako zápornou hodnotu a je porovnáno s polem **Očekávané zahájení** v pracovním příkazu. Příklad: Pokud je do tohoto pole vložena hodnota 10 a očekávané datum zahájení pracovního příkazu je od nynějška za tři dny, výsledek hodnocení bude mínus 30. Přidání výsledků 0,25 a 50 z příkladů ve výše popsaných polích **Priorita** a **Kritičnost** poskytuje celkový součet plus 20,25. Toto číslo je porovnáno se všemi ostatními skóre hodnocení pracovních příkazů během plánování pracovních příkazů a nejdříve se plánují nejvyšší skóre hodnocení.  
- **Odpovědná skupina pracovníků** - skóre hodnocení vypočtené společně s hodnotami skóre hodnocení **Skupina odpovědných pracovníků**, **Upřednostňovaný pracovník**, **Upřednostňovaná skupina pracovníků**, **Místo majetku** a **Datum zahájení**. Pokud je do tohoto pole vložena hodnota 50 a zodpovědný pracovník byl vybrán v pracovním příkazu, pracovník získá 50 bodů v celkovém výpočtu pracovníka během plánování pracovního příkazu.  
- **Skupina odpovědných pracovníků** - skóre hodnocení vypočtené společně s hodnotami skóre hodnocení **Odpovědný pracovník**, **Upřednostňovaný pracovník**, **Upřednostňovaná skupina pracovníků**, **Místo majetku** a **Datum zahájení**. Pokud je do tohoto pole vložena hodnota 50 a zodpovědný pracovník byl vybrán v pracovním příkazu, pracovník získá 50 bodů v celkovém výpočtu pracovníka během plánování pracovního příkazu.  
- **Omezit na zodpovědné** - omezuje počet pracovníků, kteří jsou k dispozici pro plánování pracovních příkazů. Pokud chcete vypočítat skóre pro všechny pracovníky bez ohledu na to, zda jsou nastaveny jako zodpovědní pracovníci nebo jako část skupiny zodpovědné pracovníků, vyberte možnost **Ne**. Chcete-li vypočítat skóre pro pracovníky, kteří jsou v pracovním příkazu nastaveni jako odpovědný pracovník, anebo zahrnuti do skupiny zodpovědných pracovníků vybrané na pracovním příkazu, vyberte možnost **Ano**.  
- **Upřednostňovaný pracovník** - skóre hodnocení vypočtené společně s hodnotami skóre hodnocení **Odpovědný pracovník**, **Upřednostňovaný pracovník**, **Upřednostňovaná skupina pracovníků**, **Místo majetku** a **Datum zahájení**. Čtyři skóre hodnocení jsou vypočítávána a spojena dohromady, aby bylo možné zadat skóre použité k výběru toho, jaký pracovník má být přiřazen ke kterému pracovnímu příkazu během plánování pracovního příkazu. Pokud je do tohoto pole vložena hodnota 10 a pracovník byl vybrán v pracovním příkazu jako upřednostňovaný pracovník, získá tento pracovník 10 bodů v celkovém výpočtu pracovníka během plánování pracovního příkazu.  
- **Upřednostňovaná skupina pracovníků** - skóre hodnocení vypočtené společně s hodnotami skóre hodnocení **Odpovědný pracovník**, **Upřednostňovaný pracovník**, **Upřednostňovaná skupina pracovníků**, **Místo majetku** a **Datum zahájení**. Pokud je do tohoto pole vložena hodnota 10 a pracovník byl přiřazen v pracovním příkazu k upřednostňované skupině pracovníků, získá tento pracovník 10 bodů v celkovém výpočtu pracovníka během plánování pracovního příkazu.  
- **Omezit na upřednostňované** - omezuje počet pracovníků, kteří jsou k dispozici pro plánování pracovních příkazů. Pokud chcete vypočítat skóre pro všechny pracovníky bez ohledu na to, zda jsou nastaveni jako upřednostňovaní pracovníci nebo jako část skupiny upřednostňovaných pracovníků, vyberte možnost **Ne**. Pokud chcete pouze vypočítat skóre pro pracovníky, kteří jsou nastaveni jako upřednostňovaní pracovníci anebo zahrnuti ve skupině upřednostňovaných pracovníků, vyberte možnost **Ano**.  
- **Místo** - skóre hodnocení vypočtené společně s hodnotami skóre hodnocení **Odpovědný pracovník**, **Upřednostňovaný pracovník**, **Upřednostňovaná skupina pracovníků**, **Místo majetku** a **Datum zahájení**. Je-li do tohoto pole vložena hodnota 3 000, pracovník získá 3 000 bodů ve výpočtu, pokud je pracovník umístěn ve stejné továrně nebo zařízení jako majetek, na kterém má být naplánována úloha.  
  - Pokud vaše společnost používá funkční místa, pracovníci dostanou plné skóre, pokud jsou umístěni na funkčním místě souvisejícím s majetkem. Pokud má funkční místo majetku nadřazený majetek, pracovníci na tomto funkčním místě dostanou 1/2 skóre. Pokud má toto místo také nadřazenou položku, pracovníci na tomto místě získají 1/3 skóre. Pokud má toto místo také nadřazenou položku, pracovníci na tomto místě získají 1/4 skóre atd.  
  - Pokud vaše společnost používá místo majetku, které nedoporučujeme, místo, oblast a zóna se používají k výpočtu skóre místa. Pracovníci dostanou plné skóre, pokud jsou umístěni v místě a oblasti a zóně související s majetkem. Pokud se místo pracovníka shoduje pouze s místem a oblastí, je skóre hodnocení pro pracovníka 2/3 plného skóre. Pokud se místo pracovníka shoduje pouze s místem, je skóre hodnocení pro pracovníka 1/3 plného skóre.  
- **Omezit na umístění** - omezuje počet pracovníků, kteří jsou k dispozici pro plánování pracovních příkazů. Chcete-li vypočítat skóre pro všechny pracovníky ve všech funkčních místech, vyberte možnost **Ne**. Chcete-li vypočítat skóre pouze pro pracovníky, kteří jsou přidruženi k funkčnímu místu pracovního příkazu, vyberte možnost **Ano**.

>[!NOTE]
>Tři pole "Omezit na" jsou zavedena ke zvýšení rychlosti plánování pracovního příkazu omezením počtu skóre vypočteného pro pracovníky.

**Počáteční datum pracovníka** - skóre hodnocení vypočtené společně s hodnotami skóre hodnocení **Odpovědný pracovník**, **Upřednostňovaný pracovník**, **Upřednostňovaná skupina pracovníků**, **Místo majetku** a **Datum zahájení**. Toto pole označuje denní skóre jako zápornou hodnotu a je porovnáno s polem **Očekávané zahájení** v pracovním příkazu. Příklad: Pokud je do tohoto pole vložena hodnota 10 a očekávané datum zahájení pracovního příkazu je zítra, výsledek hodnocení bude mínus 10.

  - Za předpokladu, že na plánovaném pracovním příkazu nebyl vybrán žádný odpovědný pracovník a skupiny odpovědných pracovníků - přidáte a odečtete hodnoty skóre hodnocení v příkladech ve výše uvedených polích **Upřednostňovaný pracovník**, **Skupina upřednostňovaných pracovníků**, **Místo majetku** a **Počáteční datum** a získáte součet 3 010. To znamená vysoké skóre pro pracovníka, který je již vybrán jako upřednostňovaný pracovník, a je zahrnut do skupiny upřednostňovaných pracovníků na pracovním příkazu, a pracovník je také umístěn ve stejném zařízení jako majetek, pro který je nutné naplánovat úlohu. To znamená, že existuje dobrá možnost, že daný pracovník bude vybrán k dokončení úlohy během plánování pracovního příkazu.  
  - Pokud je do jednoho z osmi výše uvedených polí vložena hodnota 0, nebude toto hodnocení použito během plánování pracovního příkazu.  

Odkaz **Typy dokumentů**

Vyberte typy dokumentů, které mají být k dispozici pro tisk příloh souvisejících se sestavou pracovního příkazu. To se provádí výběrem typu dokumentu v části **Dostupné** a výběrem ![šipky vpřed](media/15-setup-for-objects.png). Pokud chcete odstranit vybraný typ dokumentu, vyberte typ dokumentu v části **Vybrané** a vyberte tlačítko se ![šipkou zpět](media/16-setup-for-objects.png).

Odkaz **Číselné řady**

Vyberte požadované číselné řady v tomto oddílu. Existují dvě číselné řady pro majetek: jedna pro ručně vytvořený majetek a druhá pro majetek vytvořený prostřednictvím čekajících majetků.
