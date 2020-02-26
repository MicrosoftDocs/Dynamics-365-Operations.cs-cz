Při kopírování databáze mezi prostředími budete muset spustit nástroj opětovného zřízení prostředí předtím, než bude kopírovaná databáze plně funkční, abyste se ujistili, že jsou všechny komponenty Commerce aktuální.

> [!IMPORTANT]
> Doporučujeme spustit tento postup bez ohledu na to, zda používáte komponenty Commerce nebo ne, protože funkce Commerce je součástí všech prostředí. 

Než budete pokračovat, musíte se ujistit, že jsou splněny následující předpoklady:
1. Pokud upgradujete na vydání z července 2017 (také známé jako 7.2) 7.2.11792.56024, před spuštěním upgradu dat v tomto prostředí použijte v cílovém prostředí následující opravy aplikace hotfix X++. Zabráníte tím různým chybám, ke kterým dochází během upgradu dat:

    - KB 4036156 - Upgrade podverze aplikace Retail - Není zadána číselná řada varianty. Tento balíček oprav rovněž zahrnuje KB 4035399 a KB 4035751. Mějte na paměti, že pro použití tohoto balíčku musíte mít minimálně aktualizaci Platform Update 9. Pokud si nejste jisti, nainstalujte nejnovější binární soubory.
    
2. Pokud upgradujete z Microsoft Dynamics AX 2012, před spuštěním upgradu dat nainstalujte následující opravy aplikace hotfix X++:
    - KB 4033183 - Dynamics AX 2012 R2 nebo Dynamics AX 2012 R3 Pre-CU8 , upgrade mimo Retail se nezdařil se zprávou Objekt nebyl nalezen pro dbo.RETAILTILLLAYOUTZONE.
    - KB 4040692 - Upgrade Dynamics AX 2012 R3 na Microsoft Dynamics 365 for Operations 7.2 se nezdařil na RetailSalesLine duplicitním indexu na SalesLineIdx.
    - KB 4035490 - Problém s výkonem skriptu upgradu pole GeneralJournalAccountEntry MainAccount.


Postupujte podle těchto kroků pro spuštění nástroje opětovného zřízení prostředí.

1. V knihovně sdíleného majetku zvolte **Nasaditelný balíček softwaru**.
2. Stáhněte nástroj opětovného zřízení prostředí.
3. V knihovně majetku vašeho projektu zvolte **Nasaditelný balíček softwaru**.
4. Zvolte **Nový** pro vytvoření nového balíčku.
5. Zadejte název a popis balíčku. Jako název balíčku můžete použít **Nástroj opětovného zřízení prostředí**.
6. Načtěte balíček, který jste dříve stáhli.
7. Na stránce **Podrobnosti prostředí** pro vaše cílové prostředí zvolte **Spravovat** > **Použít aktualizace**.
8. Zvolte nástroj opětovného zřízení prostředí, který jste dříve odeslali, a poté pro použití balíčku zvolte **Použít**.
9. Sledujte průběh nasazení balíčku. 

Další informace o použití nasaditelného balíčku naleznete v tématu [Použití nasaditelného balíčku](../deployment/create-apply-deployable-package.md). Další informace o ručním použití nasaditelného balíčku naleznete v tématu [Instalace nasaditelného balíčku](../deployment/install-deployable-package.md).
