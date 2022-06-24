---
title: Povolení více způsobů vyzvednutí/doručení objednávek zákazníků
description: Tento článek vysvětluje funkci v Microsoft Dynamics 365 Commerce, která umožňuje vytvářet objednávky zákazníků k vyzvednutí v obchodě.
author: hhainesms
ms.date: 06/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 555ae3900bd7f9c66366f19a6eb2f12503898c93
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858901"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Povolení více způsobů vyzvednutí/doručení objednávek zákazníků

[!include [banner](includes/banner.md)]


V Microsoft Dynamics 365 Commerce verze 10.0.16 a novějších mohou organizace definovat více způsobů doručení, které si kupující nebo prodejní partneři mohou vybrat, když vytvoří objednávku, která bude vyzvednuta v obchodě. Tímto způsobem mohou organizace svým nakupujícím poskytnout více možností vyzvednutí. Například mnoho maloobchodníků nyní nabízí nakupujícím možnost vyzvednutí v obchodě nebo pouliční vyzvednutí objednávky. Commerce podporuje konfiguraci těchto různých způsobů vyzvednutí/doručení. Uživatelé je pak mohou využít, když vytvářejí objednávky zákazníků v jakémkoli podporovaném kanálu Commerce (elektronický obchod, kontaktní středisko nebo obchod).

## <a name="enable-and-configure-pickup-delivery-modes"></a>Povolení a konfigurace způsobů vyzvednutí/doručení

Chcete-li tuto funkci použít, zapněte **Podpora více způsobů vyzvednutí/doručení** v pracovním prostoru **Správa funkcí** v centrále Commerce. Po zapnutí této funkce je nutná další konfigurace.

V Commerce verze 10.0.15 a dřívějších mohou organizace definovat pouze jeden způsob doručení jako určený režim vyzvednutí/doručení. Tato definice se provádí na stránce **Parametry Commerce**. Ve verzi 10.0.16 a novější, když zapnete **Podpora více způsobů vyzvednutí/doručení**, způsob doručení, který byl dříve definován jako způsob vyzvednutí/doručení na stránce **Parametry Commerce** se automaticky zkopíruje do nové konfigurace pro způsoby vyzvednutí/doručení.

![Způsoby vyzvednutí/doručení na stránce Parametry Commerce.](media/multiplepickupparameter.png)

Po zapnutí funkce **Podpora více způsobů vyzvednutí/doručení** můžete definovat více způsobů vyzvednutí v mřížce **Způsob vyzvednutí dodávky** na záložce s náhledem **Způsoby doručení** na kartě **Objednávky zákazníků** na stránce **Parametry Commerce**.

Pole **Způsob doručení vyvezením** a **Elektronický způsob doručení** a možnost **U expedice objednávek zobrazit pouze možnosti způsobu dopravce** byly přemístěny na tuto kartu s náhledem.

Před konfigurací dalších způsobů vyzvednutí/doručení musíte definovat způsoby doručení. Na stránce **Způsoby doručení** v centrále Commerce přidejte způsoby doručení, které by se měly brát v úvahu jako způsoby vyzvednutí/doručení. Ujistěte se, že je veškerá konfigurace dokončena. Pokud například nabízíte u určitých obchodů pouliční výdej jako možnost doručení pro online nakupující, musíte pro tento účel vytvořit nový způsob doručení. Tento způsob doručení můžete vytvořit pomocí popisu „pouliční výdej“. Pak bude třeba zajistit, aby byl způsob doručení „pouliční výdej“ namapován na všechny obchodní kanály, které ho mohou nabízet, včetně internetových obchodů s touto možností v nabídce, a kanálů jednotlivých obchodu, které také nabízejí tuto metodu plnění. Způsoby dodání musejí být také propojeny s produkty. V tomto příkladu, pokud existují určité produkty, jejichž plnění nelze zajistit pomocí způsobu „pouliční výdej“, je třeba zajistit, aby tyto položky byly vyloučeny. Až dokončíte přidávání všech nových způsobů doručení, spusťte úlohu **Zpracovat způsoby doručení** a vytvořte tak vztahy mezi způsobem doručení, kanály a položkami. Po dokončení úlohy otevřete stránku **Plán distribuce** v centrále Commerce a spusťte úlohu distribuce **1120**, aby bylo zajištěno, že příslušné databáze kanálu Commerce budou aktualizovány s vaší novou konfigurací způsobu doručení.

![Příklad konfigurace způsobu doručení pro pouliční vyzvednutí.](media/pickupmodes.png)

Poté, co definujete další způsoby vyzvednutí/doručení, přidejte je do mřížky **Způsob vyzvednutí dodávky** na stránce **Parametry Commerce**. Poté spusťte příslušné úlohy distribuce, abyste aktualizovali příslušné databáze kanálu Commerce se změnou konfigurace.

> [!NOTE]
> Kromě stávajícího způsobu vyzvednutí/doručení, který je zkopírován do mřížky **Způsob vyzvednutí dodávky**, když zapnete **Podpora více způsobů vyzvednutí**, pro každou další konfiguraci způsobu vyzvednutí/doručení, kterou vytvoříte, byste měli nakonfigurovat nové způsoby doručení. Když přidáte způsoby doručení do mřížky **Způsob vyzvednutí dodávky**, Commerce ověří, zda se používají již nějaké aktivní otevřené řádky prodeje. Pokud jsou nalezeny otevřené řádky prodeje, zobrazí se chybová zpráva. Způsoby doručení se nepovažují za způsoby vyzvednutí/doručení, dokud nejsou uzavřeny všechny otevřené řádky prodeje, které je používají (buď fakturované, nebo zrušené).

> [!IMPORTANT]
> Poté, co definujete více než jeden způsob vyzvednutí/doručení na stránce **Parametry Commerce**, bude funkce **Podpora více způsobů vyzvednutí/doručení** povinnou a již ji nelze vypnout. Pokud musíte tuto funkci vypnout, odeberte všechny způsoby vyzvednutí/doručení kromě jednoho z mřížky **Způsob vyzvednutí dodávky**. Pokud je definován pouze jeden režim vyzvednutí/doručení, funkce již není považována za povinnou a lze ji vypnout.

### <a name="e-commerce-site-configurations"></a>Konfigurace webu elektronického obchodu

Když je zapnuta funkce **Podpora více způsobů vyzvednutí/doručení**, následující moduly na stránkách elektronického obchodu zobrazují nové způsoby vyzvednutí/doručení dle konfigurace:

- Buy box
- Selektor obchodu
- Košík
- Informace o výdeji
- Potvrzení objednávky
- Podrobnosti objednávky

K zpřístupnění způsobů vyzvednutí/doručení nejsou na stránkách elektronického obchodu nutné žádné další kroky.

## <a name="work-with-multiple-pickup-delivery-modes"></a>Použití více způsobů vyzvednutí/doručení

Když je pro kanál k dispozici více způsobů vyzvednutí/doručení, zákazníkům se při nakupování produktů, které budou vyskladněny, poskytne rozšířené prostředí. 

- V kanálech elektronického obchodování si zákazníci mohou vybrat jakýkoli platný způsob vyzvednutí/doručení, který je k dispozici. Například maloobchodník definuje dva způsoby vyzvednutí/doručení (výdej v obchodě a pouliční výdej), oba jsou nakonfigurovány v mřížce **Způsob vyzvednutí dodávky** a oba platí pro kanál plnění objednávky a produkt, který si kupující aktuálně kupuje. V takovém případě si zákazník může vybrat preferovaný způsob vyzvednutí/doručení. Vybraný způsob vyzvednutí/doručení se poté stane způsobem doručení, který je propojen s řádkem prodejní objednávky při vytvoření objednávky v centrále Commerce.

    ![Výběr možnosti vyzvednutí v elektronickém obchodu.](media/pickupecommerce.png)

- Pokud je v kanálech obchodu vytvořena objednávka zákazníka pro vyzvednutí prostřednictvím aplikace pokladního místa (POS), prodejní partner je vyzván k výběru z dostupných způsobů vyzvednutí/doručení, pokud byly nakonfigurovány. Pokud je pro kanál a položku k dispozici pouze jeden platný způsob vyzvednutí/doručení, prodejní partner není vyzván k jeho výběru. Místo toho se na řádky objednávky automaticky použije dostupný způsob vyzvednutí/doručení.

    ![Výběr možnosti vyzvednutí v aplikaci POS.](media/pickuppos.png)

- Když uživatelé v kanálech kontaktního střediska vytvoří objednávky vyzvednutí, mohou ručně vybrat libovolný definovaný způsob vyzvednutí/doručení, který je propojen s kanálem kontaktního střediska. Systém poté ověří, že vybraný způsob vyzvednutí/doručení lze použít, když je objednána položka, na kterou je odkazováno. Když je v kanálech kontaktního střediska zvolen způsob vyzvednutí/doručení, musí být řádky prodejní objednávky propojeny s platným skladem obchodu. Pokud je na řádku prodeje kontaktního střediska definován sklad bez obchodu, nelze na tomto řádku prodeje nastavit způsob vyzvednutí/doručení.
- Prodejní partneři mohou použít operaci **Stažení objednávky** nebo **Vyřízení objednávky** v aplikaci POS k načtení seznamu objednávek nebo řádků objednávek k vyzvednutí. Pokud prodejní partner použije předdefinovaný vyhledávací filtr k zobrazení všech objednávek, které budou vyzvednuty v aktuálním obchodě, budou dotazy upraveny tak, aby zajistily, že výsledky hledání budou zahrnovat všechny způsobilé objednávky, které používají jakýkoli způsob vyzvednutí/doručení. Uživatelé POS mohou také použít existující filtry k zúžení seznamu objednávek na konkrétní způsob vyzvednutí/doručení. Mohou například zobrazit pouze objednávky pro pouliční výdej.

    ![Filtr pro způsob vyzvednutí/doručení aplikovaný na seznam odvolaných objednávek.](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Úvahy nad distribuovanou správou objednávek

Funkce [distribuované správy objednávek (DOM)](./dom.md) v Commerce ignorují všechny řádky prodeje, které jsou označeny pro vyzvednutí v obchodě. Tyto funkce byly aktualizovány, aby zajistily, že řádky prodeje, které jsou propojeny s nakonfigurovanými způsoby vyzvednutí/doručení, obcházejí logiku DOM a nebudou znovu přiděleny novému skladu plnění.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
