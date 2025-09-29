<!-- version -->
pragma solidity >=0.5.0 <0.6.0;
<!-- contract -->
contract ZombieFactory {
    <!-- declare an event -->
event NewZombie(uint zombieId, string name, uint dna);

    uint dnaDigits = 16;
    uint dnaModulus = 10 ** dnaDigits;
<!-- strcuts -->
    struct Zombie {
        string name;
        uint dna;
    }

    Zombie[] public zombies;

<!--functions-->

    function _createZombie(string memory _name, uint _dna) private {
        uint id = zombies.push(Zombie(_name, _dna)) - 1;
<!-- fire an event -->
        emit NewZombie(id, _name, _dna);
    }
<!-- Private fun. with return,view -->
    function _generateRandomDna(string memory _str) private view returns (uint) {
        uint rand = uint(keccak256(abi.encodePacked(_str)));
        return rand % dnaModulus;
    }
<!-- Public fuc. -->
    function createRandomZombie(string memory _name) public {
        uint randDna = _generateRandomDna(_name);
        _createZombie(_name, randDna);
    }

}
