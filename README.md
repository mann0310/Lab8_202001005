# Lab-8_202001005
# **Name : Mann Joshi**
# **ID : 202001005**

## Creating a new Eclipse project, and within the project create a package and defining the class
![image](https://user-images.githubusercontent.com/75674065/233048296-c213e03d-6de2-42ea-ad9d-7fb66d8d7af0.png)

## Adding the Test Case

    public class BoaTest {
      Boa jen;
      Boa ken;

      @Before
      public void setUp() throws Exception {
        jen = new Boa("Jennifer", 2, "grapes");
        ken = new Boa ("Kenneth", 3, "granola bars");
      }

      @After
      public void tearDown() throws Exception {
      }

      @Test
        public void testIsHealthy() {
            assertTrue(ken.isHealthy()); // kens favourite food is granola bars
            assertFalse(jen.isHealthy());
        }

        @Test
        public void testFitsInCage() {
            assertFalse(ken.fitsInCage(2));
            assertFalse(ken.fitsInCage(3));
            assertTrue(ken.fitsInCage(5));

            assertFalse(jen.fitsInCage(1));
            assertFalse(jen.fitsInCage(2));
            assertTrue(jen.fitsInCage(3));
        }
    }
    
## Running the Test Case
![image](https://user-images.githubusercontent.com/75674065/233048462-ca422f41-c737-4e0d-8233-e570efd763ad.png)

## Adding a new method to the Boa class

	public int lengthInInches(){
		// 1 foot is 12 inches
		return this.length*12;
	}
  ![image](https://user-images.githubusercontent.com/75674065/233048700-9209c472-e485-4203-a9d3-3ff72bc6b918.png)

## Adding new test cases to test lengthInInches()

    @Test
    public void testlengthInInches() {
    	assertEquals("error in lengthInInches()",  36, ken.lengthInInches());
    	assertNotEquals("error in lengthInInches()",  35, ken.lengthInInches());
        
    	assertEquals("error in lengthInInches()",  24, jen.lengthInInches());
    	assertNotEquals("error in lengthInInches()",  30, jen.lengthInInches());
    }
    
## Running the new Test Case
![image](https://user-images.githubusercontent.com/75674065/233048916-75330595-e08b-4388-aaab-7b8c2f28e913.png)
