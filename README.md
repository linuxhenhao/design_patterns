# design_patterns

All those are learning from derek's design_patterns video serials [youtube channel](https://www.youtube.com/playlist?list=PLF206E906175C7E07) 

1. strategy pattern:
    * a list of similar algorithms, implement every one in a seperate class
    * attach one of the implemented class's instance to our running class
    * may need dynamic change (not necessary)

    example:
    
    ```java
    class Test {
        private Strategy strategy;
        public Test(Strategy strategy) {
            this.strategy = strategy;
        }    
        
        public void trySpark() {
            System.out.println(strategy.spark());
        }

        public void setStrategy(Strategy strategy) {
            # changing working behavior dynamicly       
            this.strategy = strategy;
        }
    }

    Interface Strategy {
        public string spark();
    }

    class DogStrategy implements Strategy {
        @override
        public string spark() {
            return "Wang Wang";
        }
    }

    class CatStrategy implements Strategy {
        @override
        public string spark() {
            return "Miao Miao";
        }
    }
    ```

